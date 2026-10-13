# Página de Políticas de Privacidade

Hub público com as Políticas de Privacidade dos aplicativos Android publicados.
Cada app tem sua própria página (`<app>.html`) e o `index.html` lista todas.

## Publicação (GitHub Pages)

Este repositório foi pensado para ser publicado como **`<usuario>.github.io`**
(ex.: `danielbdelfino.github.io`), ficando disponível em:

```
https://danielbdelfino.github.io/
```

Passos:

1. Crie no GitHub um repositório **público** chamado `danielbdelfino.github.io`.
2. Envie os arquivos para a branch `main`.
3. Vá em **Settings → Pages → Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** / pasta **/ (root)**
4. Em alguns minutos o site estará no ar. A URL da política do SafeView será:
   `https://danielbdelfino.github.io/safeview.html`

> **Importante:** GitHub Pages em repositórios **privados** exige plano GitHub Pro.
> Para manter o site gratuito, o repositório do Pages deve ser **público**
> (o código dos apps pode continuar em repositórios privados separados).

## Como adicionar a política de um novo app

1. Copie `modelo.html` para `nome-do-app.html`.
2. Preencha os campos `NOME_DO_APP`, `DATA_DE_VIGENCIA`, `SEU_EMAIL` e o conteúdo.
3. No `index.html`, adicione um card dentro de `<div class="apps">`:

```html
<a class="app-card" href="nome-do-app.html">
  <div class="name">Nome do App</div>
  <div class="desc">Descrição curta.</div>
</a>
```

4. Preencha o campo **URL da Política de Privacidade** no Google Play Console com o link do app.

## Estrutura

```
.
├── index.html        # lista de apps
├── safeview.html     # política do SafeView
├── modelo.html       # template para novos apps
├── assets/style.css  # estilos
└── .nojekyll         # desativa o processamento Jekyll
```
