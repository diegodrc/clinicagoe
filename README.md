# GOE — Grupo Odontológico Especializado

Landing page estática para a clínica GOE Odontologia 24h — Belo Horizonte, MG.

## Tecnologias

- HTML5 semântico
- CSS3 (variáveis, grid, flexbox, responsivo mobile-first)
- JavaScript vanilla (IntersectionObserver, scroll suave, menu mobile)
- Google Fonts (Poppins + Playfair Display)

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
