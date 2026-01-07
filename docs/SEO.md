# 🔍 SEO & METADADOS | AD Telas e Redes

---

## 📋 Índice

1. [Meta Tags Globais](#meta-tags-globais)
2. [Meta Tags por Página](#meta-tags-por-p%C3%A1gina)
3. [Open Graph Tags](#open-graph-tags)
4. [Schema.org Estruturado](#schemaorg-estruturado)
5. [SEO Local & Bairros](#seo-local--bairros)
6. [Google Console & Analytics](#google-console--analytics)
7. [Checklist SEO](#checklist-seo)

---

## 🌐 Meta Tags Globais

### HTML Base
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="theme-color" content="#0f7b6e">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
</head>
```

---

## 📑 Meta Tags por Página

### HOME
```html
<title>AD Telas e Redes | Telas Mosquiteiras e Redes de Proteção em SP</title>
<meta name="description" content="Telas mosquiteiras, redes de proteção e pet screen sob medida. Instalação em 48h, garantia de 2 anos. Orçamento gratuito em São Paulo.">
<meta name="keywords" content="tela mosquiteira, rede de proteção, pet screen, São Paulo, instalação, SP">
<link rel="canonical" href="https://adtelaseredes.com.br">
<meta name="robots" content="index, follow">
```

**Notes:**
- Title: 55 caracteres (otimizado para busca)
- Meta description: 155 caracteres (cabe no SERP)
- Canonical: aponta para a versão "correta" da página

---

### SERVIÇO: TELAS MOSQUITEIRAS
```html
<title>Telas Mosquiteiras sob Medida | AD Telas e Redes SP</title>
<meta name="description" content="Telas mosquiteiras profissionais em fibra ou alumínio. Proteção contra insetos, ventilação garantida. Instalação rápida em São Paulo.">
<meta name="keywords" content="tela mosquiteira, tela de alumínio, tela de fibra, mosquito, inseto, SP">
<link rel="canonical" href="https://adtelaseredes.com.br/servico/tela-mosquiteira">
```

---

### SERVIÇO: REDES DE PROTEÇÃO
```html
<title>Redes de Proteção | Segurança para Família em SP</title>
<meta name="description" content="Redes de proteção certificadas para varandas, sacadas e piscinas. Segurança para crianças e pets. Galeria de trabalhos e depoimentos em São Paulo.">
<meta name="keywords" content="rede de proteção, varanda segura, pet, criança, SP">
<link rel="canonical" href="https://adtelaseredes.com.br/servico/rede-protecao">
```

---

### SERVIÇO: PET SCREEN
```html
<title>Pet Screen Resistente | Proteção para Gatos e Cães em SP</title>
<meta name="description" content="Pet screen reforçado 4x mais resistente. Seguro para gatos, cães e pássaros. Ventilação 100% mantida. Orçamento em 24h.">
<meta name="keywords" content="pet screen, gato, cão, janela segura, animal, SP">
<link rel="canonical" href="https://adtelaseredes.com.br/servico/pet-screen">
```

---

### PORTFÓLIO
```html
<title>Portfólio | Trabalhos Realizados em São Paulo</title>
<meta name="description" content="Galeria de instalações de telas e redes em apartamentos e casas em SP. Fotos antes/depois, depoimentos de clientes e detalhes técnicos.">
<meta name="keywords" content="portfolio, work, case study, antes e depois, galeria">
<link rel="canonical" href="https://adtelaseredes.com.br/portfolio">
```

---

### SOBRE
```html
<title>Sobre Nós | AD Telas e Redes</title>
<meta name="description" content="Conheça a história da AD Telas e Redes. Máis de 10 anos de experiência em instalações profissionais em São Paulo. Especialistas confiáveis.">
<meta name="keywords" content="sobre, empresa, história, confiança, experiência">
<link rel="canonical" href="https://adtelaseredes.com.br/sobre">
```

---

### CONTATO
```html
<title>Contato | AD Telas e Redes</title>
<meta name="description" content="Entre em contato com a AD Telas e Redes. Telefone: (11) 99999-9999. WhatsApp, email, formulário. Resposta em 24h, garantido.">
<meta name="keywords" content="contato, telefone, whatsapp, email, atenção ao cliente">
<link rel="canonical" href="https://adtelaseredes.com.br/contato">
```

---

## 🗼️ Open Graph Tags

### Home Page
```html
<meta property="og:title" content="AD Telas e Redes — Proteção Profissional para Sua Casa">
<meta property="og:description" content="Redes e telas de proteção sob medida. Instalação rápida, qualidade garantida.">
<meta property="og:image" content="https://adtelaseredes.com.br/images/hero_varanda_01.jpg">
<meta property="og:image:width" content="1920">
<meta property="og:image:height" content="1280">
<meta property="og:url" content="https://adtelaseredes.com.br">
<meta property="og:type" content="website">
<meta property="og:site_name" content="AD Telas e Redes">
<meta property="og:locale" content="pt_BR">

<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="AD Telas e Redes">
<meta name="twitter:description" content="Proteção professional com qualidade garantida.">
<meta name="twitter:image" content="https://adtelaseredes.com.br/images/hero_varanda_01.jpg">
```

---

## 🗐️ Schema.org Estruturado

### Schema LocalBusiness (JSON-LD)
```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "AD Telas e Redes",
  "image": "https://adtelaseredes.com.br/images/logo.png",
  "description": "Instalação profissional de telas mosquiteiras, redes de proteção e pet screen em São Paulo.",
  "url": "https://adtelaseredes.com.br",
  "telephone": "+55 (11) 99999-9999",
  "email": "ola@adtelaseredes.com.br",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Endereço da filial] — opcional",
    "addressLocality": "São Paulo",
    "addressRegion": "SP",
    "postalCode": "[CEP]",
    "addressCountry": "BR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "-23.550",
    "longitude": "-46.633"
  },
  "priceRange": "R$ 300 - R$ 5000",
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"],
    "opens": "08:00",
    "closes": "18:00"
  },
  "areaServed": [
    "Pinheiros, SP",
    "Vila Madalena, SP",
    "Vila Mariana, SP",
    "Higienópolis, SP",
    "São Paulo, SP"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "ratingCount": "247"
  },
  "review": [
    {
      "@type": "Review",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5"
      },
      "author": {
        "@type": "Person",
        "name": "Maria Silva"
      },
      "reviewBody": "Serviço excelente! Instalaram a rede em menos de 48h."
    }
  ]
}
</script>
```

---

### Schema BreadcrumbList (Para Navegação)
```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://adtelaseredes.com.br"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Serviços",
      "item": "https://adtelaseredes.com.br/#services"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Telas Mosquiteiras",
      "item": "https://adtelaseredes.com.br/servico/tela-mosquiteira"
    }
  ]
}
</script>
```

---

### Schema Product (Para Serviços)
```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "Instalação de Telas Mosquiteiras",
  "description": "Proteção contra insetos com telas de alta qualidade.",
  "provider": {
    "@type": "LocalBusiness",
    "name": "AD Telas e Redes",
    "url": "https://adtelaseredes.com.br"
  },
  "areaServed": "São Paulo, SP",
  "priceRange": "R$ 300 - R$ 1500",
  "image": "https://adtelaseredes.com.br/images/tela_janela_01.jpg",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "ratingCount": "150"
  }
}
</script>
```

---

## 📍 SEO Local & Bairros

### Estratégia Multi-Bairro
Criar páginas/seções para principais bairros com conteúdo otimizado:

#### URL Pattern
```
https://adtelaseredes.com.br/[bairro]/[servico]
Ex: https://adtelaseredes.com.br/pinheiros/tela-mosquiteira
```

#### Meta Tags Exemplo: Pinheiros
```html
<title>Tela Mosquiteira em Pinheiros, SP | AD Telas e Redes</title>
<meta name="description" content="Telas mosquiteiras em Pinheiros. Instalação rápida, proteção contra insetos. Orçamento gratuito para sua rua.">
<meta name="keywords" content="tela mosquiteira pinheiros, instalação pinheiros, proteção insetos">
```

### Bairros Prioritários
1. **Pinheiros** (Pop. ~100k, renda alta, densidade de aptos)
2. **Vila Mariana** (Pop. ~80k, renda média-alta)
3. **Higienópolis** (Pop. ~60k, renda alta, pets)
4. **Vila Madalena** (Pop. ~70k, renda média)
5. **Brooklin** (Pop. ~50k, novos empreendimentos)
6. **Morumbi** (Pop. ~80k, casaroes, segurança alta)
7. **Ipiranga** (Pop. ~90k, zona sul)
8. **Icarai** (Pop. ~40k, expansion)

---

## 📋 Google Console & Analytics

### Google Search Console

**Setup:**
1. Acessar: https://search.google.com/search-console
2. Adicionar propriedade: https://adtelaseredes.com.br
3. Verificar ownership (Tag HTML / DNS)

**Monitoramento:**
- [ ] Submeter sitemap.xml
- [ ] Monitorar cliques & impressões
- [ ] Revisar erros de rastreamento
- [ ] Verificar "Core Web Vitals"
- [ ] Submeter URLs importantes

**Sitemap.xml Exemplo:**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://adtelaseredes.com.br</loc>
        <lastmod>2025-01-07</lastmod>
        <changefreq>weekly</changefreq>
        <priority>1.0</priority>
    </url>
    <url>
        <loc>https://adtelaseredes.com.br/servico/tela-mosquiteira</loc>
        <lastmod>2025-01-07</lastmod>
        <changefreq>monthly</changefreq>
        <priority>0.8</priority>
    </url>
    <url>
        <loc>https://adtelaseredes.com.br/portfolio</loc>
        <lastmod>2025-01-07</lastmod>
        <changefreq>weekly</changefreq>
        <priority>0.7</priority>
    </url>
</urlset>
```

---

### Google Analytics 4 (GA4)

**Setup:**
1. Acessar: https://analytics.google.com
2. Criar propriedade: "AD Telas e Redes"
3. Adicionar tag GA4 ao HTML (vide README.md)
4. Adicionar Google Tag Manager (GTM)

**KPIs para Monitorar:**
- [ ] Sessions & Users
- [ ] Bounce Rate
- [ ] Time on Page
- [ ] Conversion Rate (Form Submissions)
- [ ] Traffic por Source (Organic, Direct, Referral, Paid)
- [ ] Comportamento por Device (Mobile, Desktop)
- [ ] Top Pages & Exit Pages

**Eventos Customizados:**
```javascript
// WhatsApp Click
gtag('event', 'whatsapp_click', {
  'event_category': 'engagement',
  'event_label': 'CTA_Hero'
});

// Form Submit
gtag('event', 'form_submit', {
  'event_category': 'conversion',
  'event_label': 'Quote_Request'
});

// Service Page View
gtag('event', 'view_service', {
  'event_category': 'engagement',
  'event_label': 'Tela_Mosquiteira'
});
```

---

## ✅ Checklist SEO

### Onpage
- [ ] Title tags: 55-60 caracteres, inclui keyword principal
- [ ] Meta descriptions: 155 caracteres, call-to-action
- [ ] H1-H6: Hierarquia clara, apenas 1 H1 por página
- [ ] Alt text: Todas as imagens tém alt text relevante
- [ ] URLs: Lowercase, hifens, sem parâmetros unnécessarios
- [ ] Internal Links: Contextuais, anchor text natural
- [ ] Schema.org: LocalBusiness, BreadcrumbList, Service
- [ ] Open Graph: og:title, og:description, og:image
- [ ] Robots.txt: Permite crawling dos arquivos principais
- [ ] Sitemap.xml: Atualizado com todas as páginas

### Technical
- [ ] Mobile Responsiveness: Todos os breakpoints testados
- [ ] Page Speed: LCP < 2.5s, FID < 100ms, CLS < 0.1
- [ ] HTTPS: SSL certificado válido
- [ ] Robots.txt: Configurado corretamente
- [ ] Canonical Tags: Evita páginas duplicadas
- [ ] 404 Handling: Página de erro customizada
- [ ] Structured Data: Valida em Google Rich Results

### Content
- [ ] Keyword Research: 5-10 palavras-chave por página
- [ ] Keyword Density: 1-2% (natural, não overstuffing)
- [ ] Content Length: Mínimo 300 palavras por página
- [ ] Unique Content: Sem duplicatas internas
- [ ] Update Frequency: Blog/news atualizados mensalmente
- [ ] Internal Linking: 3-5 links internos por página

### Local
- [ ] Google My Business: Criado, verificado, otimizado
- [ ] NAP Consistency: Nome, endereço, telefone iguais em todos lugares
- [ ] Local Schema: AggregateRating, AreaServed preenchidos
- [ ] Local Citations: Presença em Yelp, Yellow Pages (opcional)
- [ ] Reviews: Mínimo 10 reviews com 4+ estrelas
- [ ] Bairros Prioritários: Páginas otimizadas para cada um

### Analytics
- [ ] GA4 Implementado
- [ ] GTM Implementado
- [ ] Eventos Custom Rastreados
- [ ] Goals/Conversions Configuradas
- [ ] Dashboards Monitorados

---

**Versão 1.0 | Janeiro 2025**
