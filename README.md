# 🎯 AD Telas e Redes | Website Redesign

**Versão:** 1.0.0  
**Data de Criação:** Janeiro 2025  
**Autor:** Full-Stack Design Team

---

## 📋 Índice

1. [Visão Geral do Projeto](#vis%C3%A3o-geral-do-projeto)
2. [Estrutura de Diretórios](#estrutura-de-diret%C3%B3rios)
3. [Setup & Instalação](#setup--instala%C3%A7%C3%A3o)
4. [Arquivos de Configuração](#arquivos-de-configura%C3%A7%C3%A3o)
5. [Guia de Imagens](#guia-de-imagens)
6. [Copy & Microcopy](#copy--microcopy)
7. [SEO & Metadados](#seo--metadados)
8. [Integrações](#integra%C3%A7%C3%B5es)
9. [Performance & Acessibilidade](#performance--acessibilidade)
10. [Guia para Fotógrafo](#guia-para-fot%C3%B3grafo)

---

## 🎨 Visão Geral do Projeto

### Objetivo
Redesign profissional, mobile-first e altamente conversível do website institucional da **AD Telas e Redes** — empresa de telas mosquiteiras, redes de proteção e pet screen em São Paulo.

### Estilo & Tom
**"Local Service Premium"** → Limpo, confiável, profissional. Visual moderno que inspira confiança em serviços técnicos.

### Paleta de Cores
```
🟦 Primária (Teal): #0f7b6e (Confiança)
🟨 Accent Warm: #e67e3c (CTAs — Urgência)
⚪ Neutro: #ffffff (Fundo)
⬜ Texto: #1f2937 (Dark)
```

### Tipografia
- **Heading Font:** Poppins (Bold, Semibold)
- **Body Font:** Inter (Regular, Medium)

---

## 📁 Estrutura de Diretórios

```
ad-telas-redes-website/
├── index.html                 # Home page completa
├── pages/
│   ├── servico-tela.html     # Página de serviço: Telas Mosquiteiras
│   ├── servico-rede.html     # Página de serviço: Redes de Proteção
│   ├── servico-petscreen.html# Página de serviço: Pet Screen
│   ├── portfolio.html         # Galeria filtrável de trabalhos
│   ├── sobre.html             # Página Sobre
│   └── contato.html           # Página de Contato / Atendimento
├── images/                    # Pasta de imagens (18+ ativos)
│   ├── hero_varanda_01.jpg    # 1920x1280 | Hero background
│   ├── tela_janela_01.jpg     # 1200x900 | Tela mosquiteira
│   ├── petscreen_gato_01.jpg  # 1200x900 | Pet screen
│   ├── antes_depois_*.jpg     # 1200x900 | Antes/Depois
│   ├── avatar_*.jpg           # 400x400 | Fotos de depoentes
│   └── ... (mais 10-15 imagens)
├── assets/
│   ├── design-system.css      # Design tokens & estilos reutilizáveis
│   ├── icons.svg              # Ícones SVG em sprite
│   ├── colors.json            # Paleta exportável (HEX)
│   ├── typography.css         # Definições de fontes
│   └── animations.css         # Transições & keyframes
├── js/
│   ├── main.js                # Lógica de interatividade
│   ├── analytics.js           # Google Analytics + GTM
│   ├── form-handler.js        # Validação & envio de formulários
│   └── lightbox.js            # Galer ia de imagens
├── docs/
│   ├── COPY.md                # Headlines, CTAs, descrições
│   ├── SEO.md                 # Meta tags, Schema.org
│   ├── PHOTOSHOOT_BRIEF.md    # Guia para fotógrafo
│   └── IMPLEMENTATION.md      # Checklist de implementação
└── README.md                  # Este arquivo
```

---

## 🚀 Setup & Instalação

### Pré-requisitos
- Node.js 16+ (para build tools — opcional)
- Git
- Editor de código (VS Code recomendado)
- Navegador moderno (Chrome, Firefox, Safari, Edge)

### Passos Rápidos

```bash
# 1. Clonar repositório
git clone https://github.com/conta2secunndaria-ship-it/ad-telas-redes-website.git
cd ad-telas-redes-website

# 2. Abrir em servidor local (sem dependências)
cd project-root
python -m http.server 8000
# ou com npx
npx http-server

# 3. Acessar
open http://localhost:8000
```

### Build & Deploy (Opcional — Com Webpack/Vite)

```bash
# Instalar dependências
npm install

# Build para produção
npm run build

# Deploy
npm run deploy
```

---

## ⚙️ Arquivos de Configuração

### `.env.local` (Criar manualmente)
```env
# Google Analytics
VITE_GA_MEASUREMENT_ID=G-XXXXXXX

# WhatsApp Business API (opcional)
VITE_WHATSAPP_API_KEY=sua_chave_aqui

# Email para formulários
VITE_FORM_EMAIL=ola@adtelaseredes.com.br

# CRM Integration (HubSpot / Zapier)
VITE_ZAPIER_WEBHOOK=https://hooks.zapier.com/hooks/catch/xxxxx

# Telefone
VITE_WHATSAPP_NUMBER=5511999999999
```

### `colors.json` (Paleta Exportável)
```json
{
  "primary": "#0f7b6e",
  "primary-dark": "#065d55",
  "primary-light": "#1aa89d",
  "accent-warm": "#e67e3c",
  "accent-warm-dark": "#d46f2a",
  "neutral-white": "#ffffff",
  "neutral-light": "#f8f9fa",
  "neutral-gray": "#6b7280",
  "neutral-dark": "#1f2937",
  "text-primary": "#111827",
  "text-secondary": "#6b7280",
  "success": "#10b981",
  "error": "#ef4444"
}
```

---

## 🖼️ Guia de Imagens

### Convenção de Naming
```
[PREFIX]_[DESCRICAO]_[NUMERO].[EXT]

Exemplos:
hero_varanda_01.jpg
service_tela_mosquiteira_02.jpg
portfolio_antes_depois_pinheiros_01_before.jpg
portfolio_antes_depois_pinheiros_01_after.jpg
avatar_cliente_maria_silva.jpg
```

### Lista Mínima de Ativos (18 imagens)

| Arquivo | Proporção | Alt Text | Caption SEO |
|---------|-----------|----------|-------------|
| `hero_varanda_01.jpg` | 16:9 (1920×1280) | Rede de proteção instalada em varanda de apartamento em São Paulo | Rede instalada em varanda — segurança para imóveis em SP |
| `tela_janela_01.jpg` | 4:3 (1200×900) | Tela mosquiteira para janela residencial | Tela mosquiteira sob medida para janelas |
| `petscreen_gato_01.jpg` | 4:3 (1200×900) | Pet screen resistente para proteção de gatos | Pet Screen: proteção resistente para pets |
| `antes_depois_varanda_01_before.jpg` | 4:3 (1200×900) | Antes: varanda sem proteção | Antes da instalação |
| `antes_depois_varanda_01_after.jpg` | 4:3 (1200×900) | Depois: varanda com rede instalada | Depois da instalação |
| `instalacao_equipe_01.jpg` | 4:3 (1200×900) | Equipe profissional instalando redes de proteção | Instalação profissional com equipe treinada |
| `instalacao_detalhe_fibra.jpg` | 4:3 (1200×900) | Close-up de material resistente (fibra de vidro) | Material de alta qualidade: fibra de vidro resistente |
| `janela_basculante_antes.jpg` | 4:3 (1200×900) | Janela basculante antes da tela | Janela aberta — sem proteção |
| `janela_basculante_depois.jpg` | 4:3 (1200×900) | Janela basculante com tela mosquiteira | Tela mosquiteira instalada |
| `porta_correr_01.jpg` | 4:3 (1200×900) | Porta de correr com tela | Tela para porta de correr |
| `crianca_janela_segura.jpg` | 4:3 (1200×900) | Criança perto de janela protegida com rede | Segurança para crianças: rede de proteção |
| `gato_petscreen.jpg` | 4:3 (1200×900) | Gato brincando junto a pet screen | Pet screen: seu gato em segurança |
| `cachorro_varanda.jpg` | 4:3 (1200×900) | Cachorro em varanda com rede de proteção | Pets em segurança: rede certificada |
| `avatar_maria.jpg` | 1:1 (400×400) | Foto perfil de cliente — Maria Silva | Cliente satisfeito: Pinheiros, SP |
| `avatar_joao.jpg` | 1:1 (400×400) | Foto perfil de cliente — João Santos | Cliente satisfeito: Vila Mariana, SP |
| `avatar_ana.jpg` | 1:1 (400×400) | Foto perfil de cliente — Ana Costa | Cliente satisfeito: Higienópolis, SP |
| `fachada_apartamento.jpg` | 4:3 (1200×900) | Prédio residencial com redes e telas instaladas | Redes em prédio residencial — discretas e eficientes |
| `loja_materiais.jpg` | 4:3 (1200×900) | Estoque de materiais (rolo de tela, alumínio) | Materiais premium em estoque |

### Especificações Técnicas

**Resolução:**
- Hero: 1920×1280 (16:9)
- Galeria: 1200×900 (4:3)
- Avatares: 400×400 (1:1)

**Formato:** JPG (80-85% quality) + WEBP para navegadores modernos

**Otimização:**
- Compressão: TinyJPG / ImageOptim
- Tamanho máximo: 200KB por imagem
- Responsive: Usar `srcset` e `<picture>`

**Srcset Exemplo:**
```html
<img src="/images/hero_varanda_01.jpg"
     srcset="/images/hero_varanda_01-sm.jpg 600w,
             /images/hero_varanda_01-md.jpg 1000w,
             /images/hero_varanda_01.jpg 1920w"
     sizes="(max-width: 600px) 100vw,
            (max-width: 1200px) 90vw,
            1920px"
     alt="Rede de proteção instalada em varanda de apartamento em São Paulo"
     loading="lazy">
```

---

## 📝 Copy & Microcopy

### Headlines (Testar 3 Variações A/B)

**Variação 1 (Segurança - Conversão Alta)**
```
"Proteja sua família com redes e telas sob medida"
```

**Variação 2 (Urgência + Facilidade)**
```
"Instalação em 48h | Segurança garantida | Sem dor de cabeça"
```

**Variação 3 (Benefício Direto)**
```
"Seu apartamento seguro e ventilado | Sem mosquitos, sem preocupação"
```

### Subheading
```
"Instalação rápida — orçamento em 24h — garantia de 2 anos"
```

### CTAs Primários (3 Variações)

**Variação 1 (Direto)**
```
"Solicitar Orçamento via WhatsApp"
```

**Variação 2 (Urgência)**
```
"Quero meu orçamento em 24h"
```

**Variação 3 (Conversação)**
```
"Falar com especialista no WhatsApp"
```

### Descrições de Serviço

**Telas Mosquiteiras**
- **Descrição 1 (Técnica):** Proteção contra mosquitos, insetos voadores e ácaros. Disponível em fibra de vidro (mais durável) ou alumínio (mais leve). Mantém a ventilação natural de seu imóvel.
- **Descrição 2 (Benefício):** Durma tranquilo sem moscas ou mosquitos. Abra suas janelas sem medo, respire ar fresco e puro — 100% protegido.
- **Descrição 3 (Social Proof):** Escolhida por 5.000+ clientes em SP. Durabilidade comprovada: garantia de 2 anos contra defeitos de fabricação.

**Redes de Proteção**
- **Descrição 1 (Segurança):** Certificação técnica internacional. Resistem a quedas, impactos e intempéries. Ideais para varandas, sacadas, piscinas e áreas com crianças ou pets.
- **Descrição 2 (Paz de Espírito):** Durma sabendo que sua família está segura. Redes discretas que não prejudicam a ventilação nem a vista da sua varanda.
- **Descrição 3 (ROI):** Aumenta o valor de revenda do imóvel. Aprovada por incorporadoras e condomínios de luxo em São Paulo.

**Pet Screen**
- **Descrição 1 (Técnica):** Material reforçado 4x mais resistente que tela comum. Suporta patas de gatos, unhas de cães e até mordidas.
- **Descrição 2 (Tranquilidade):** Seu gato pode ficar na janela sem risco de escapar. Ventilação completa, sem prejudicar a visão nem a entrada de luz.
- **Descrição 3 (Diferencial):** Único serviço em SP com pet screen colorido. Combina com sua decoração e ainda protege quem você ama.

---

## 🔍 SEO & Metadados

### Meta Tags - Home
```html
<meta name="title" content="AD Telas e Redes | Telas Mosquiteiras e Redes de Proteção em SP">
<meta name="description" content="Telas mosquiteiras, redes de proteção e pet screen sob medida. Instalação em 48h, garantia de 2 anos. Orçamento gratuito em São Paulo.">
<meta name="keywords" content="tela mosquiteira, rede de proteção, pet screen, São Paulo, SP">
<meta property="og:title" content="AD Telas e Redes — Proteção Profissional para Sua Casa">
<meta property="og:description" content="Redes e telas sob medida. Instalação rápida, qualidade garantida.">
<meta property="og:image" content="/images/hero_varanda_01.jpg">
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://adtelaseredes.com.br">
```

### Schema.org LocalBusiness
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "AD Telas e Redes",
  "description": "Instalação de telas mosquiteiras, redes de proteção e pet screen em São Paulo",
  "url": "https://adtelaseredes.com.br",
  "telephone": "+55 (11) 99999-9999",
  "email": "ola@adtelaseredes.com.br",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "São Paulo",
    "addressRegion": "SP",
    "addressCountry": "BR"
  },
  "areaServed": [
    "Pinheiros",
    "Vila Madalena",
    "Vila Mariana",
    "Higienópolis",
    "Zona Sul de SP"
  ],
  "image": "/images/hero_varanda_01.jpg",
  "priceRange": "R$ 300 - R$ 5000",
  "ratingValue": "4.8",
  "ratingCount": "247"
}
```

### SEO Local — Bairros
Criar páginas/seções para bairros principais:
- Telas Mosquiteiras em Pinheiros
- Redes de Proteção em Vila Mariana
- Pet Screen em Higienópolis
- etc.

---

## 🔗 Integrações

### WhatsApp Click-to-Chat

```javascript
const whatsAppNumber = '5511999999999';
const message = 'Olá, quero orçamento para [SERVIÇO] — bairro: [BAIRRO]';
const whatsAppURL = `https://wa.me/${whatsAppNumber}?text=${encodeURIComponent(message)}`;
window.open(whatsAppURL, '_blank');
```

### Formulário → Email + CRM

**Fluxo:**
1. Usuário preenche formulário (Nome, Telefone, Bairro, Serviço)
2. JavaScript valida dados
3. POST para `/api/form-submit` (seu servidor)
4. Webhook Zapier envia para HubSpot / Integração CRM
5. Email automático de confirmação para cliente

**Endpoint Exemplo (Node/Express):**
```javascript
app.post('/api/form-submit', async (req, res) => {
  const { name, phone, neighborhood, service } = req.body;
  
  // Validar
  if (!name || !phone) {
    return res.status(400).json({ error: 'Dados incompletos' });
  }

  // Enviar para CRM via Zapier
  await fetch(process.env.ZAPIER_WEBHOOK, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ name, phone, neighborhood, service, timestamp: new Date() })
  });

  // Enviar email
  await sendEmail(phone, `Obrigado ${name}! Responderemos em 24h.`);

  res.json({ success: true });
});
```

### Google Analytics + GTM

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXX', {
    'page_title': document.title,
    'page_path': window.location.pathname
  });
</script>

<!-- Google Tag Manager -->
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
 new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-XXXXXXX');</script>
```

---

## ⚡ Performance & Acessibilidade

### Checklist de Performance (Lighthouse)

- [ ] **Score ≥ 90 Mobile** (Performance)
- [ ] **Score ≥ 90 Desktop**
- [ ] CLS < 0.1 (Cumulative Layout Shift)
- [ ] LCP < 2.5s (Largest Contentful Paint)
- [ ] FID < 100ms (First Input Delay)
- [ ] TTL < 3s (Time to Largest Contentful Paint)

### Otimizações

1. **Imagens:**
   - [ ] Usar WEBP + JPG fallback
   - [ ] Lazy loading (`loading="lazy"`)
   - [ ] Responsive images (`srcset`)
   - [ ] Compressão otimizada (<200KB)

2. **CSS/JS:**
   - [ ] Minificar e comprimir
   - [ ] Remover CSS não utilizado
   - [ ] Defer JS não-crítico
   - [ ] Inline CSS crítico (<14KB)

3. **Cache:**
   - [ ] Service Worker para offline
   - [ ] Cache headers HTTP (max-age)
   - [ ] CDN para imagens (Cloudflare / Bunny)

### Acessibilidade (WCAG 2.1 AA)

- [ ] **Contraste:** Mínimo 4.5:1 em textos
- [ ] **Navegação:**
  - [ ] Todos botões têm `aria-label` ou texto visible
  - [ ] Ordem de tab lógica
  - [ ] Indicador visual de foco
- [ ] **Imagens:**
  - [ ] Alt text em todas as imagens
  - [ ] Caption em imagens funcionais
- [ ] **Formulários:**
  - [ ] Labels associados a inputs (`<label for="id">`)
  - [ ] Validação acessível
  - [ ] Mensagens de erro claras
- [ ] **Cores:**
  - [ ] Não confiar apenas em cor
  - [ ] Suporte a modo escuro
- [ ] **Mobile:**
  - [ ] Toque mínimo de 44×44px
  - [ ] Escala de texto responsiva

---

## 📷 Guia para Fotógrafo

### Brief de Fotografia

**Objetivo:** Criar 18–20 fotos profissionais que sirvam como referência para substit uição das imagens fictícias.

### Ângulos & Cenários Essenciais

#### 1. Seção Hero (3 fotos)
- **Varanda com rede:** Ângulo 45°, luz natural tarde (golden hour), destaca segurança + ventilação
- **Janela com tela:** Luz frontal, mostra detalhe da malha + ventilação
- **Porta de entrada:** Exterior + Interior (split screen possível), detalha instalação

#### 2. Antes/Depois (6 fotos — 3 pares)
- Varanda: Antes (sem proteção) → Depois (com rede)
- Janela: Antes (aberta, sem tela) → Depois (com tela mosquiteira)
- Porta: Antes (standard) → Depois (com tela/rede)

**Requisitos:**
- Mesmo ângulo, mesma luz natural
- Destaque para a transformação visual
- Fotos tiradas no mesmo imóvel ou simulado

#### 3. Processo Instalação (3 fotos)
- Equipe em ação (sem rostos em close, ou desfocados)
- Detalhe: Soldadura/ajustes na malha
- Ferramental profissional em ação

#### 4. Close-up Material (2 fotos)
- Fibra de vidro (textura, detalhe)
- Alumínio (ajustes, qualidade)

#### 5. Segurança (3 fotos)
- Criança perto de janela protegida
- Gato brincando junto a pet screen
- Cachorro em varanda com rede (movimento, naturalidade)

#### 6. Contexto Residencial (3 fotos)
- Fachada de prédio com redes/telas instaladas
- Ambiente interno (sala com varanda protegida)
- Estoque/vitrine de materiais

#### 7. Avatares / Depoentes (3 fotos)
- Foto de perfil: Maria Silva, 40-50 anos, estilo executivo
- Foto de perfil: João Santos, 30-40 anos, casual
- Foto de perfil: Ana Costa, 25-35 anos, descontraído

### Especificações Técnicas

**Câmera Recomendada:**
- DSLR ou mirrorless (Canon R5, Sony A7III, Nikon Z6)
- Lente: 24-70mm f/2.8 (versátil)

**Iluminação:**
- Natural (luz solar): Melhor entre 8-10h ou 16-18h (luz dourada)
- Refletor branco (se necessário, para sombras)
- Não usar flash direto em produtos — luz natural é premium

**Pós-Produção:**
- Corte final: 1920×1280 (hero), 1200×900 (galeria), 400×400 (avatares)
- Cor grading: Saturação natural +10%, contraste +15%
- Remover imperfeições menores
- Exportar em JPG (85% quality) + WEBP

**Cronograma Estimado:**
- Planejamento: 1 semana
- Fotografia em campo: 2 dias (múltiplos imóveis, horários variados)
- Pós-produção: 1 semana
- **Total: 2-3 semanas**

### Referências de Estilo

- **Inspiração 1:** Squarespace Home Services templates (limpo, profissional)
- **Inspiração 2:** Houzz photos (contexto real, qualidade premium)
- **Inspiração 3:** Capa de design premium (cores neutras, detalhe em foco)

---

## ✅ Checklist de Implementação

### Fase 1: Setup Técnico
- [ ] Clonar repositório
- [ ] Configurar `.env.local`
- [ ] Testar em localhost (8000)
- [ ] Validar HTML/CSS (W3C Validator)

### Fase 2: Imagens
- [ ] Preparar 18 imagens fictícias (placeholders Unsplash/Generated)
- [ ] Otimizar para web (TinyJPG)
- [ ] Criar srcset para cada imagem
- [ ] Adicionar alt text + caption
- [ ] [POSTERIOR] Substituir por fotos reais do cliente

### Fase 3: Copy & SEO
- [ ] Revisar todos os textos (ortografia, tom)
- [ ] Adicionar meta tags
- [ ] Implementar Schema.org LocalBusiness
- [ ] Validar em Google Rich Results Test

### Fase 4: Integrações
- [ ] WhatsApp Click-to-Chat funcionando
- [ ] Formulário validando e enviando
- [ ] Email automático configurado
- [ ] Google Analytics conectado
- [ ] GTM implementado

### Fase 5: Testing
- [ ] Teste mobile (iPhone, Android)
- [ ] Teste tablet (iPad)
- [ ] Teste desktop (Chrome, Firefox, Safari, Edge)
- [ ] Teste de formulário (envio real)
- [ ] Teste de acessibilidade (axe DevTools, Wave)
- [ ] Teste de performance (Lighthouse: ≥90)
- [ ] Teste de SEO (Screaming Frog, SEMrush)

### Fase 6: Deploy
- [ ] Build para produção
- [ ] Deploy em staging
- [ ] Teste completo em URL de staging
- [ ] Deploy em produção
- [ ] Monitorar erros (Sentry, Google Console)
- [ ] Validar indexação Google

### Fase 7: Post-Launch
- [ ] Monitorar analytics (GA4)
- [ ] A/B test CTAs (variações de headlines)
- [ ] Coletar feedback de clientes
- [ ] Iteração & melhorias contínuas

---

## 📞 Suporte & Contato

**Dúvidas técnicas?**
- 📧 Email: dev@adtelaseredes.com.br
- 🐙 GitHub: [ad-telas-redes-website](https://github.com/conta2secunndaria-ship-it/ad-telas-redes-website)
- 💬 WhatsApp: (11) 99999-9999

---

**Versão 1.0 | Janeiro 2025 | © AD Telas e Redes**
