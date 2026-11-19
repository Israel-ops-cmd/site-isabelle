# Site Isabelle Salustino

Site estático (HTML, CSS e JS num único `index.html`), sem etapa de build.

## Rodar localmente
Na pasta do projeto:

```
npx serve .
```
ou, com Python instalado:
```
python -m http.server 8000
```
Depois abra http://localhost:3000 (serve) ou http://localhost:8000 (Python).
Abrir o `index.html` direto no navegador também funciona, mas a rolagem e as fontes se comportam melhor com servidor.

## Estrutura
- `index.html`: página inteira, com CSS e JS embutidos
- `img/`: fotos em WebP (800/1600px; recortes 700/1200px)
- `vendor/`: GSAP 3.12.5, ScrollTrigger 3.12.5 e Lenis 1.1.13 (versões fixas, servidas pelo próprio site)
- `favicon.svg`, `apple-touch-icon.png`, `og-image.jpg` (1200x630, preview no WhatsApp)
- `vercel.json`: URLs limpas e cache longo para `/img` e `/vendor`

## Publicar
O repositório no GitHub está ligado à Vercel (Framework Preset: Other, Build Command vazio, Output Directory `./`).
Cada push na branch `main` publica sozinho.

Ao trocar de domínio, atualize no `index.html`: `<link rel="canonical">`, `og:url`, `og:image`, `twitter:image` e o `url`/`image` do JSON-LD.

## Trocar fotos
Substitua os arquivos em `img/` mantendo os mesmos nomes e proporções. Originais tratados ficam fora do repositório (`fotos-tratadas/`, `fotos-escolhidas/`).
