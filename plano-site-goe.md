# Plano de Criação — Landing Page GOE Odontologia
> Documento para uso com agente de IA (ex: Claude Code, Cursor, v0, etc.)

---

## 1. Visão Geral do Projeto

**Cliente:** GOE — Grupo Odontológico Especializado  
**Site atual:** https://www.clinicagoe.com.br  
**Entrega:** Landing page estática em HTML/CSS/JS puro (sem framework, sem build step)  
**Deploy:** Cloudflare Pages — basta fazer push de arquivos estáticos para um repositório Git conectado ao Cloudflare Pages. Nenhuma configuração adicional é necessária além do arquivo `index.html` na raiz.

**Objetivo:** Substituir o site WordPress atual por uma landing page moderna, rápida, responsiva e com fácil manutenção — hospedada gratuitamente no Cloudflare Pages.

---

## 2. Estrutura de Arquivos

```
/
├── index.html
├── style.css
├── script.js
└── README.md
```

Tudo em **um único diretório, sem subpastas**. O agente deve gerar os três arquivos principais.

---

## 3. Seções da Landing Page (ordem de cima para baixo)

### 3.1 — Navbar (fixa no topo)
- Logo à esquerda: `https://clinicagoe.com.br/wp-content/uploads/2021/08/goe-clinica-odontologia-24h-bh-2.png`
- Links de navegação (scroll suave para âncoras): Sobre, Especialidades, Tecnologia, Equipe, Convênios, Contato
- Botão CTA de urgência no canto direito: **"Urgência 24h"** → link WhatsApp
- Em mobile: menu hambúrguer

### 3.2 — Hero
- **Headline:** "Cuidando do seu sorriso e bem-estar 24h por dia"
- **Subtítulo:** "A GOE Odontologia é referência em BH em implantodontia, harmonização facial e atendimento de urgência a qualquer hora."
- Dois botões CTA:
  - **"Agendar consulta"** → WhatsApp
  - **"Atendimento de Urgência"** → WhatsApp (destaque diferente)
- Imagem de fundo (hero background): `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/background_slide-3.jpg`
- Imagem alternativa de slide disponível: `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/SLIDE_CLINICAGOE2-1.jpg`

### 3.3 — Sobre a Clínica (`id="sobre"`)
- **Título:** "Sobre a GOE"
- **Texto:**
  > "Nascida em 2009, a GOE Odontologia 24 Horas foi fundada pela Dra. Renata Zampa e pelo Dr. Marcus Iori com o propósito de oferecer atendimento completo, humano e acessível a qualquer hora. Nossa missão é promover saúde, autoestima e transformar sorrisos com tecnologia e excelência."
- Imagem decorativa da clínica: `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/h3-slider-image-2-550x550-500x500.png`
- 3 cards de destaque com ícone + número + descrição:
  - 🦷 **+15 anos** de experiência
  - 🏆 **Atendimento 24h** todos os dias
  - 😊 **Tecnologia CEREC** restaurações em 1 consulta

### 3.4 — Especialidades (`id="especialidades"`)
- **Título:** "Nossas Especialidades"
- Grid de 3×2 cards (responsivo: 1 coluna mobile, 2 tablet, 3 desktop)
- Cada card: imagem de capa + nome da especialidade + breve descrição

| Especialidade | Descrição | Imagem |
|---|---|---|
| Odontologia | Estudo e tratamento dos dentes, boca e ossos da face | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/odontologia.jpg` |
| Periodontia | Cuidado dos tecidos que suportam os dentes, como gengiva e osso alveolar | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/periodontia.jpg` |
| Prevenção | Correção e manutenção da saúde periodontal com controle clínico | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/prevencao.jpg` |
| Implantodontia | Implantes com materiais modernos para suporte de próteses | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/implantodontia.jpg` |
| Reabilitação Oral | Restauração completa da saúde bucal com técnicas avançadas | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/reabilitacao_oral.jpg` |
| Ortodontia | Correção do alinhamento dos dentes | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/Ortodontia.jpg` |

### 3.5 — Tecnologia CEREC (`id="tecnologia"`)
- **Título:** "Tecnologia CEREC MC XL"
- **Subtítulo:** "Restaurações em cerâmica em uma única consulta"
- **Texto:**
  > "A GOE possui o sistema exclusivo CEREC MC XL — tecnologia CAD/CAM que cria inlays, onlays, coroas e facetas em cerâmica pura na cor do dente, sem metal, em uma única visita. Sem provisórios, sem segunda consulta."
- **Lista de benefícios:**
  - ✅ Apenas uma consulta necessária
  - ✅ Cerâmica da cor do dente — invisível
  - ✅ Alta resistência e durabilidade
  - ✅ Sem metal, biocompatível
  - ✅ Resultado estético superior
- **Vídeo do YouTube incorporado** (iframe responsivo):
  ```
  https://www.youtube.com/embed/F6kwMFZiTLk?feature=oembed
  ```
- Imagem da máquina CEREC: `https://clinicagoe.com.br/wp-content/uploads/2018/03/cerecmx.jpg`

### 3.6 — Equipe (`id="equipe"`)
- **Título:** "Conheça Nossa Equipe"
- **Subtítulo:** "Profissionais altamente qualificados e prontos para cuidar de você"
- Cards lado a lado com foto circular, nome, especialidade e mini bio

| Nome | Título | Bio resumida | Foto |
|---|---|---|---|
| Dra. Renata Camargos Zampa | Especialista em Harmonização Facial, Periodontia e Ortodontia | Une saúde e estética para elevar a autoestima com naturalidade e procedimentos personalizados. | *(não encontrada no site atual — usar placeholder ou imagem da clínica)* |
| Dr. Marcus Ricardo Iori | Mestre em Prótese Dentária, Especialista em Implantodontia | Referência em Implantodontia e Reabilitação Oral, alia inovação ao sistema CEREC para resultados excepcionais. | `https://www.clinicagoe.com.br/wp-content/uploads/2016/03/marcus-quad-scaled.jpg` |
| Dr. Márcio Hamacek Dias | Especialista em Endodontia e Dentística | Pós-graduado em Endodontia, Biossegurança, Dentística e Odontologia do Trabalho. | `https://www.clinicagoe.com.br/wp-content/uploads/2018/03/dr-marcio.png` |
| Dra. Raissa Resende Alves Neves | Especialista em Endodontia | Pós-Graduada em Endodontia, atendimento cuidadoso e preciso. | `https://www.clinicagoe.com.br/wp-content/uploads/2017/04/dra-rayssa.png` |

### 3.7 — Depoimentos
- **Título:** "O que nossos pacientes dizem"
- 3 cards de depoimentos (carousel simples em mobile, grid em desktop):
  1. *"Sou cliente da clínica há mais de 10 anos. Os dentistas são profissionais sérios e competentes. Já indiquei para vários amigos e todos ficaram muito satisfeitos."*
  2. *"Fico muito feliz em ser cliente da GOE. Dr. Marcus e Dra. Renata são realmente encantadores e excelentes profissionais."*
  3. *"Há 4 anos sou cliente da GOE e não tenho nenhuma reclamação a fazer! Todos os profissionais são bem preparados e muito educados."*

### 3.8 — Convênios (`id="convenios"`)
- **Título:** "Convênios Aceitos"
- Grid de logos de convênios (lazy load via `loading="lazy"`)
- Lista de imagens de convênios disponíveis no servidor:

```
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/abberta-saude.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/geap.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/marinha.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/odontosystem.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/unna.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/usisaude.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/allsaude.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/goldental.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/medgold.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/plan-assiste.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/caixa.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/amil-medial.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/hapvida.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/metlife.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/porto-seguro.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/sociodonto.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/bradesco-dental.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/inpao.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/odontolife.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/postal-saude.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/sul-america-dental.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/unimed-odonto.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/interodonto.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2018/01/odonto-empresas.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/dental-uni.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/ipsm.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/odonto-industria.jpg
https://www.clinicagoe.com.br/wp-content/uploads/2021/08/rede-brasil-dental.jpg
```

### 3.9 — Contato e CTA Final (`id="contato"`)
- **Título:** "Agende sua Consulta"
- **Texto:** "Entre em contato agora pelo WhatsApp ou ligue para nós. Atendemos 24 horas para urgências."
- Três botões grandes:
  - 📱 **WhatsApp** → `https://wa.me/553192920507?text=Olá, gostaria de agendar uma consulta na GOE`
  - 📞 **Telefone** → `tel:+553132236342` (número: (31) 3223-6342)
  - 📍 **Localização** → link Google Maps para "GOE Odontologia Av. do Contorno Belo Horizonte"
- Mapa incorporado (opcional): Google Maps embed da clínica

### 3.10 — Footer
- Logo pequena da GOE
- Links rápidos para as seções
- Redes sociais:
  - Instagram: `https://www.instagram.com/goeodontologia/`
  - WhatsApp: `https://wa.me/553192920507`
- Endereço: Av. do Contorno — Belo Horizonte, MG
- Texto: © 2025 GOE Grupo Odontológico Especializado

---

## 4. Identidade Visual

### 4.1 Paleta de Cores
Baseada no site atual com refinamento moderno:

```css
:root {
  /* Cores principais */
  --color-primary: #0282d8;      /* Azul GOE — cor principal do site */
  --color-primary-dark: #006bb5; /* Azul mais escuro para hover/ênfase */
  --color-accent: #00b4d8;       /* Azul turquesa — para detalhes e destaques */

  /* Neutros */
  --color-white: #ffffff;
  --color-off-white: #f4f5fb;    /* Fundo de seções alternadas */
  --color-light-gray: #eeeeee;
  --color-dark: #1a2332;         /* Texto principal — quase preto azulado */
  --color-text-muted: #5a6a7a;   /* Texto secundário */

  /* CTAs */
  --color-cta-primary: #0282d8;
  --color-cta-whatsapp: #25D366; /* Verde WhatsApp */
  --color-cta-urgency: #e63946;  /* Vermelho urgência */
}
```

### 4.2 Tipografia
Importar do Google Fonts:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
```

- **Títulos (H1, H2):** `Playfair Display` — elegante, transmite confiança e premium
- **Corpo, botões, nav:** `Poppins` — moderno, legível, sem serifa
- **Tamanhos:**
  - H1 Hero: `clamp(2.5rem, 5vw, 4rem)`
  - H2 Seção: `clamp(1.8rem, 3vw, 2.5rem)`
  - Body: `1rem` / `1.6` line-height
  - Small/Caption: `0.875rem`

*(Nota: O site atual já usa Poppins via Cloudflare Fonts — manter essa família é coerente com a identidade)*

### 4.3 Estilo Visual
- **Tom:** Profissional e confiável, mas com calor humano — não frio/clínico demais
- **Bordas:** `border-radius: 12px` nos cards; `border-radius: 50px` nos botões
- **Sombras:** Suaves, `box-shadow: 0 4px 24px rgba(2, 130, 216, 0.12)`
- **Seções:** Alternar fundo branco (`#fff`) e cinza suave (`#f4f5fb`)
- **Hero:** Overlay escuro semitransparente sobre a foto de fundo (texto legível)
- **Separadores de seção:** Ondas SVG suaves entre seções (opcional, mas recomendado)

---

## 5. Comportamentos e Interatividade (JavaScript puro)

- **Scroll suave** para âncoras ao clicar nos links da navbar
- **Navbar sticky** que muda de aparência (background + sombra) ao fazer scroll
- **Menu mobile** hambúrguer com animação de abertura/fechamento
- **Animações de entrada** nas seções ao entrar no viewport (`IntersectionObserver`) — fade-in + slide-up
- **Cards de especialidade** com hover: leve elevação + sombra azul
- **Seção de convênios:** scroll horizontal automático (marquee) em mobile
- **Botão flutuante de WhatsApp** fixo no canto inferior direito em todas as telas
- **Vídeo YouTube** carregado com `loading="lazy"` via iframe

---

## 6. SEO e Performance (para Cloudflare Pages)

```html
<!-- No <head> do index.html -->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="GOE Odontologia 24 Horas em Belo Horizonte. Especialistas em Implantodontia, Harmonização Facial, CEREC e urgências 24h. Agende sua consulta.">
<meta property="og:title" content="GOE — Grupo Odontológico Especializado | Odontologia 24h BH">
<meta property="og:description" content="Clínica odontológica 24 horas em BH. Implantodontia, CEREC, Harmonização Facial e atendimento de urgência.">
<meta property="og:image" content="https://clinicagoe.com.br/wp-content/uploads/2021/08/goe-clinica-odontologia-24h-bh-2.png">
<meta property="og:url" content="https://www.clinicagoe.com.br/">
<link rel="canonical" href="https://www.clinicagoe.com.br/">
<title>GOE — Grupo Odontológico Especializado | Odontologia 24h em BH</title>
```

- Todas as imagens com `loading="lazy"` exceto hero e logo
- CSS crítico inline no `<head>`, restante em `style.css`
- Sem frameworks externos — apenas HTML, CSS e JS vanilla
- **Sem Node.js, sem npm, sem build step** — compatível direto com Cloudflare Pages

---

## 7. Deploy no Cloudflare Pages

**Instrução para o agente incluir no README.md:**

```markdown
## Deploy no Cloudflare Pages

1. Suba os arquivos para um repositório GitHub (público ou privado)
2. Acesse https://dash.cloudflare.com → Workers & Pages → Create application → Pages
3. Conecte o repositório GitHub
4. Configurações de build:
   - Framework preset: **None**
   - Build command: *(deixar em branco)*
   - Build output directory: `/` (raiz)
5. Clique em "Save and Deploy"
6. O site estará live em `*.pages.dev` em menos de 1 minuto
7. Para domínio customizado: Settings → Custom Domains → adicionar `clinicagoe.com.br`
```

---

## 8. Assets de Referência — Resumo

### Logos
| Uso | URL |
|---|---|
| Logo principal (fundo claro) | `https://clinicagoe.com.br/wp-content/uploads/2021/08/goe-clinica-odontologia-24h-bh-2.png` |
| Logo alternativa (escura) | `https://clinicagoe.com.br/wp-content/uploads/2018/01/goe-logo-1-1.png` |
| Logo mobile | `https://clinicagoe.com.br/wp-content/uploads/2021/08/goe-clinica-odontologia-24h-bh1.png` |

### Imagens de Fundo / Hero
| Uso | URL |
|---|---|
| Hero background principal | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/background_slide-3.jpg` |
| Hero alternativo | `https://www.clinicagoe.com.br/wp-content/uploads/2018/01/SLIDE_CLINICAGOE2-1.jpg` |
| Header sorriso | `https://clinicagoe.com.br/wp-content/uploads/2018/01/header_sorriso.jpg` |

### Vídeo YouTube
| Conteúdo | URL embed |
|---|---|
| Demonstração CEREC MC XL | `https://www.youtube.com/embed/F6kwMFZiTLk` |
| Link direto YouTube | `https://www.youtube.com/watch?v=F6kwMFZiTLk` |

### Contatos
| Canal | Dado |
|---|---|
| WhatsApp | `https://wa.me/553192920507` |
| Telefone | `(31) 3223-6342` |
| Instagram | `https://www.instagram.com/goeodontologia/` |
| Endereço | Av. do Contorno — Belo Horizonte, MG |

---

## 9. Checklist Final para o Agente

- [ ] `index.html` na raiz com toda a estrutura semântica e âncoras corretas
- [ ] `style.css` com variáveis CSS, responsividade mobile-first, media queries para tablet e desktop
- [ ] `script.js` com scroll suave, navbar sticky, menu mobile, IntersectionObserver para animações, e botão flutuante WhatsApp
- [ ] `README.md` com instruções de deploy no Cloudflare Pages
- [ ] Todas as imagens com `alt` descritivo e `loading="lazy"` (exceto hero/logo)
- [ ] Iframe do YouTube com `loading="lazy"` e wrapper responsivo (`aspect-ratio: 16/9`)
- [ ] Botão flutuante de WhatsApp fixo no canto inferior direito
- [ ] Meta tags SEO completas no `<head>`
- [ ] Testar breakpoints: 375px (mobile), 768px (tablet), 1280px (desktop)
- [ ] Sem dependências externas além de Google Fonts
