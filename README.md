# Via Forte Incorporadora — Site Institucional

Site institucional de página única (single-page) da **Via Forte Incorporadora**, apresentando os empreendimentos de alto padrão no Espírito Santo: **Tallinn Smart Living**, **Vila Paradiso** e **Galle**.

Construído em HTML, CSS e JavaScript puro (sem framework). Os formulários de contato direcionam o lead para o WhatsApp.

## Estrutura

```
index.html        # Página completa (markup + CSS + JS inline)
assets/           # Imagens (logo + fotos dos empreendimentos)
  logo.png
  tallinn.png
  paradiso.png
  galle.png
package.json      # Script de start (servidor estático)
```

## Rodar localmente

```bash
npm install
npm start
```

Ou, sem instalar nada, sirva a pasta com qualquer servidor estático:

```bash
npx serve .
```

Depois abra o endereço indicado no terminal (ex.: `http://localhost:3000`).

## Formulários → WhatsApp

Os dois formulários ("Quero acesso antecipado" e "Quero ser contactado") montam uma
mensagem e abrem o WhatsApp **(27) 99246-8344**. O número fica definido na constante
`WA` no bloco de script ao final do `index.html`.

## Personalização rápida

| O que mudar | Onde |
|---|---|
| Número de WhatsApp | constante `WA` no `<script>` final do `index.html` |
| Domínio (SEO / compartilhamento) | tags `canonical` e `og:`/`twitter:` no `<head>` |
| Imagem de compartilhamento (WhatsApp/Facebook) | `og:image` no `<head>` |
| Empreendimentos (textos, fotos, galeria) | objeto `projects` no `<script>` do `index.html` |

## Deploy

Qualquer hospedagem de site estático serve (Vercel, Netlify, Cloudflare Pages,
GitHub Pages, Render). É só publicar o conteúdo da pasta — não há build.
