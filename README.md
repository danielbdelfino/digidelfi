# DigiDelfi — Políticas de Privacidade

Site (GitHub Pages) da **DigiDelfi**, uma software house independente de aplicativos Android.
Reúne a página institucional e as Políticas de Privacidade de cada app (exigidas pela Google Play).

- Hub: `index.html`
- SafeView: `safeview.html`
- Template para novos apps: `modelo.html`

## Publicação (GitHub Pages)

Publicado como repositório **`digidelfi.github.io`**, disponível em:

```
https://digidelfi.github.io/
```

Passos (caso precise reproduzir):

1. Crie no GitHub um repositório **público** chamado `digidelfi.github.io`.
2. Envie os arquivos para a branch `main`.
3. Em **Settings → Pages → Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** / pasta **/ (root)**
4. O site fica no ar em alguns minutos.

> GitHub Pages em repositórios **privados** exige plano GitHub Pro. Para manter gratuito,
> o repositório do Pages deve ser **público** (o código dos apps pode continuar privado).

## Como adicionar a política de um novo app

1. Copie `modelo.html` para `nome-do-app.html` e preencha os campos/conteúdo.
2. Copie o ícone do app para `assets/` (ex.: `assets/nome-do-app-icon.png`).
3. No `index.html`, adicione um card dentro de `<div class="apps">`:

```html
<a class="app-card" href="nome-do-app.html">
  <img src="assets/nome-do-app-icon.png" alt="Ícone do Nome do App" />
  <div>
    <div class="name">Nome do App</div>
    <div class="desc">Descrição curta.</div>
    <div class="tags"><span class="tag">Categoria</span></div>
  </div>
  <div class="arrow">→</div>
</a>
```

4. Preencha o campo **URL da Política de Privacidade** no Google Play Console com o link do app
   (ex.: `https://digidelfi.github.io/nome-do-app.html`).

## Estrutura

```
.
├── index.html            # página inicial (institucional + lista de apps)
├── safeview.html         # política do SafeView
├── modelo.html           # template para novos apps
├── assets/
│   ├── logo.svg          # marca DigiDelfi
│   ├── safeview-icon.png # ícone do SafeView
│   └── style.css         # estilos
└── .nojekyll             # desativa o processamento Jekyll
```
