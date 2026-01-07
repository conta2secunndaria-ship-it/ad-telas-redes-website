# ⚙️ GUIA DE IMPLEMENTAÇÃO | AD Telas e Redes

**Status:** Ready to Deploy  
**Last Updated:** Janeiro 2025

---

## 📄 Índice

1. [Fase 1: Setup Local](#fase-1-setup-local)
2. [Fase 2: Integrações](#fase-2-integrações)
3. [Fase 3: Testing](#fase-3-testing)
4. [Fase 4: Deploy](#fase-4-deploy)
5. [Fase 5: Monitoramento](#fase-5-monitoramento)
6. [Troubleshooting](#troubleshooting)

---

## 🚀 Fase 1: Setup Local

### Pré-requisitos
```bash
# Verificar Node.js
node --version  # v16+ recomendado

# Verificar Git
git --version   # 2.30+

# Verificar NPM
npm --version   # 7+
```

### Instalar Projeto Localmente

```bash
# 1. Clonar repositório
git clone https://github.com/conta2secunndaria-ship-it/ad-telas-redes-website.git
cd ad-telas-redes-website

# 2. Instalar dependências
npm install

# 3. Copiar variáveis de ambiente
cp .env.example .env.local

# 4. Preencher .env.local
# (vide seção Configuração abaixo)

# 5. Iniciar servidor de desenvolvimento
npm run dev

# Acessar: http://localhost:3000
```

### Configuração de Variáveis de Ambiente

Arquivo: `.env.local` (NÃO commitar este arquivo!)

```env
# Analytics
VITE_GA_MEASUREMENT_ID=G-XXXXXXX
VITE_GTM_ID=GTM-XXXXXXX

# WhatsApp
VITE_WHATSAPP_NUMBER=5511999999999
VITE_WHATSAPP_MESSAGE_TEMPLATE="Olá, quero orçamento para [SERVIÇO]"

# Email
VITE_SMTP_HOST=smtp.seuservidor.com
VITE_SMTP_PORT=587
VITE_SMTP_USER=seu_email@seudominio.com
VITE_SMTP_PASSWORD=sua_senha_segura
VITE_FORM_EMAIL=ola@adtelaseredes.com.br

# CRM Integration (Zapier / HubSpot)
VITE_ZAPIER_WEBHOOK=https://hooks.zapier.com/hooks/catch/[ID]/...
VITE_HUBSPOT_PORTAL_ID=123456
VITE_HUBSPOT_API_KEY=seu_api_key

# Modo Produção
VITE_APP_ENV=development  # ou 'production'
VITE_APP_URL=http://localhost:3000
```

---

## 🔗 Fase 2: Integrações

### 2.1 WhatsApp Click-to-Chat

**Status:** ✅ Pronto (Implementado no HTML)

**Testar:**
```javascript
// No console do navegador
const wa = new URLSearchParams();
wa.set('text', 'Olá, quero orçamento para Telas Mosquiteiras');
window.open(`https://wa.me/5511999999999?${wa}`, '_blank');
```

---

### 2.2 Formulário → Email + Zapier

**Setup Zapier:**

1. Acessar: https://zapier.com
2. Criar novo Zap
3. Trigger: "Webhook" (When a POST is made to a URL...)
4. Colocar URL do Webhook gerada em: `VITE_ZAPIER_WEBHOOK`
5. Actions:
   - Send Email (Gmail / Outlook)
   - Add CRM Record (HubSpot / Pipedrive)
   - Send Slack Message (opcional)

**Exemplo de Payload (Form):**
```json
{
  "name": "Maria Silva",
  "phone": "11 99999-9999",
  "email": "maria@email.com",
  "neighborhood": "Pinheiros",
  "service": "Redes de Proteção",
  "notes": "Tenho criança pequena",
  "timestamp": "2025-01-07T19:30:00Z",
  "source": "website_form"
}
```

**Implementação no Backend (Node/Express):**

```javascript
// routes/api/forms.js
const express = require('express');
const axios = require('axios');
const router = express.Router();

router.post('/quote-request', async (req, res) => {
  try {
    const { name, phone, neighborhood, service, notes } = req.body;

    // Validar
    if (!name || !phone) {
      return res.status(400).json({ error: 'Dados incompletos' });
    }

    // Sanitizar telefone
    const cleanPhone = phone.replace(/\D/g, '');

    // Payload para Zapier
    const payload = {
      name,
      phone: cleanPhone,
      neighborhood,
      service,
      notes,
      timestamp: new Date().toISOString(),
      source: 'website_form',
      ip: req.ip
    };

    // Enviar para Zapier
    await axios.post(process.env.VITE_ZAPIER_WEBHOOK, payload);

    // Resposta ao cliente
    res.json({
      success: true,
      message: 'Orçamento solicitado com sucesso!',
      id: Date.now()
    });

  } catch (error) {
    console.error('Erro ao processar formulário:', error);
    res.status(500).json({ error: 'Erro ao processar solicitação' });
  }
});

module.exports = router;
```

---

### 2.3 Google Analytics + GTM

**Instalar GA4:**

1. Acessar: https://analytics.google.com
2. Criar propriedade: "AD Telas e Redes"
3. Copiar ID da medição: `G-XXXXXXX`
4. Adicionar a `.env.local`: `VITE_GA_MEASUREMENT_ID`
5. Validar em DevTools (Network > https://www.google-analytics.com)

**Instalar GTM:**

1. Acessar: https://tagmanager.google.com
2. Criar Container: "ad-telas-redes"
3. Copiar ID: `GTM-XXXXXXX`
4. Validar implementação com Google Tag Assistant

**Eventos Recomendados:**

```javascript
// Page View (automático com GA4)
gtag('event', 'page_view');

// Click em CTA WhatsApp
gtag('event', 'whatsapp_click', {
  'event_category': 'engagement',
  'event_label': 'CTA_Hero'
});

// Form Submit
gtag('event', 'form_submit', {
  'event_category': 'conversion',
  'event_label': 'Quote_Request'
});

// View Serviço
gtag('event', 'view_service', {
  'event_category': 'engagement',
  'event_label': 'Tela_Mosquiteira'
});

// Abrir Galeria
gtag('event', 'view_gallery', {
  'event_category': 'engagement',
  'event_label': 'Portfolio'
});
```

---

## 🔍 Fase 3: Testing

### 3.1 Teste Manual (Mobile)

**Dispositivos Testar:**
- [ ] iPhone 12 / 13 / 14
- [ ] Samsung Galaxy A50 / S21
- [ ] iPad Pro
- [ ] iPad Mini

**Checklist:**
- [ ] Hero carrega corretamente
- [ ] Serviços cards responsívos
- [ ] Galeria antes/depois carrega
- [ ] CTA flutuante visível no mobile
- [ ] Formulário submite sem erros
- [ ] WhatsApp abre corretamente
- [ ] Imagens carregam rapidamente (lazy load funciona)

### 3.2 Teste de Performance

```bash
# Rodas Lighthouse
npm run lighthouse

# Esperado:
# ✅ Performance: ≥ 90
# ✅ Accessibility: ≥ 90
# ✅ Best Practices: ≥ 90
# ✅ SEO: ≥ 95
```

### 3.3 Teste de Acessibilidade

**Tools:**
- [ ] axe DevTools (Chrome Extension)
- [ ] WAVE (WebAIM)
- [ ] Lighthouse Accessibility

**Verificar:**
- [ ] Contraste mínimo 4.5:1
- [ ] Labels em formulários
- [ ] Alt text em imagens
- [ ] Navegação por teclado funciona
- [ ] Focus indicators visíveis

### 3.4 Teste de SEO

```bash
# Usar Screaming Frog (local)
# ou verificar manualmente:

# Meta tags
grep -n "<meta" index.html

# Canonical
grep -n "canonical" index.html

# Schema.org
grep -n "application/ld+json" index.html

# Estrutura H1-H6
grep -n "<h[1-6]" index.html
```

---

## 📄 Fase 4: Deploy

### 4.1 Escolher Hosting

**Opções Recomendadas:**

| Plataforma | Preco | Facilidade | Ideal Para |
|-----------|-------|-----------|------------|
| **Vercel** | $20/m | ⭐⭐⭐⭐⭐ | Frontend + Functions |
| **Netlify** | $19/m | ⭐⭐⭐⭐ | Frontend statico |
| **GitHub Pages** | FREE | ⭐⭐⭐ | Frontend statico |
| **AWS Amplify** | $0-100/m | ⭐⭐ | Full-stack |
| **DigitalOcean** | $5-12/m | ⭐⭐⭐ | Full-stack |

**Recomendação: Vercel** (melhor para Next.js/Vue.js + API routes)

### 4.2 Deploy em Vercel

```bash
# 1. Instalar Vercel CLI
npm i -g vercel

# 2. Login
vercel login

# 3. Deploy
vercel

# 4. Configurar variáveis de ambiente
vercel env add VITE_GA_MEASUREMENT_ID
vercel env add VITE_WHATSAPP_NUMBER
# ... (adicionar todas)

# 5. Deploy em produção
vercel --prod
```

### 4.3 Setup de Domínio

**Registrar Domínio:**
- Registrar `adtelaseredes.com.br` em Registro.br ou Godaddy

**Apontar DNS:**
1. Acessar painel de hospedagem
2. Encontrar "Registros DNS" ou "Name Servers"
3. Configurar:
   ```
   A Record: 76.76.19.165 (Vercel)
   CNAME: www.adtelaseredes.com.br -> adtelaseredes.com.br
   ```

**SSL Certificate:**
- Vercel ativa automaticamente (Let's Encrypt)

### 4.4 Verificar Deploy

```bash
# Testar acesso
curl -I https://adtelaseredes.com.br

# Esperado:
# HTTP/2 200
# X-Powered-By: Vercel
```

---

## 📈 Fase 5: Monitoramento

### 5.1 Monitorar Performance

**Ferramentas:**
- [ ] Google Analytics 4 (sessions, users, conversions)
- [ ] Google Search Console (impressions, CTR, ranking)
- [ ] Sentry (error tracking)
- [ ] UptimeRobot (página online 24/7)

**Setup Uptime Monitor:**
```bash
# Ir para https://uptimerobot.com
# Criar monitor:
# URL: https://adtelaseredes.com.br
# Frequency: Every 5 minutes
# Notifications: Email + Slack
```

### 5.2 Backup & Versionamento

```bash
# Manter backup mensal
git tag v1.0.0
git push origin v1.0.0

# Criar release no GitHub
# https://github.com/conta2secunndaria-ship-it/ad-telas-redes-website/releases
```

### 5.3 Atualizaciones de Conteúdo

**Semestral:**
- [ ] Revisar copy e headlines
- [ ] Atualizar fotos (sazonalidade)
- [ ] Adicionar novos depoimentos
- [ ] Revisar FAQ

**Mensal:**
- [ ] Revisar analytics
- [ ] Verificar erros em Search Console
- [ ] Responder feedback de clientes

---

## 🚫 Troubleshooting

### Problema: "CORS Error" ao submeter formulário

**Solução:**
```javascript
// Adicionar headers CORS no backend
app.use((req, res, next) => {
  res.header('Access-Control-Allow-Origin', '*');
  res.header('Access-Control-Allow-Methods', 'GET, POST, PUT, DELETE');
  res.header('Access-Control-Allow-Headers', 'Content-Type');
  next();
});
```

### Problema: Imagens não carregam

**Solução:**
1. Verificar path (relativo vs absoluto)
2. Verificar se arquivos existem em `/public/images`
3. Usar URLs absolutas para deploy
```javascript
<img src="https://adtelaseredes.com.br/images/hero.jpg" />
```

### Problema: WhatsApp abre mas não envia mensagem

**Solução:**
1. Verificar número do WhatsApp (com código país)
2. Verificar encoding da mensagem (UTF-8)
3. Testar em outro navegador/device

### Problema: GA4 não registra eventos

**Solução:**
1. Verificar ID de medição
2. Verificar firewall/adblocker
3. Aguardar 24h para dados aparecerem no GA

---

**Versão 1.0 | Janeiro 2025 | Suporte: dev@adtelaseredes.com.br**
