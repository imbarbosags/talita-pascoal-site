# Dra. Talita Pascoal | Pilates Clínico

Site de uma página, estático (HTML, CSS e JavaScript em um único `index.html`). Não precisa de build.

## Arquivos

- `index.html` — a página inteira (estrutura, estilos e animações)
- `hero.jpg` — foto da abertura
- `anel.jpg` — foto do bloco "Quem conduz"
- `logo-roxa.svg`, `logo-branca.svg` — logo nas duas cores
- `.nojekyll` — faz o GitHub Pages servir os arquivos como estão

## Ver no computador

Abra a pasta no VS Code e use a extensão **Live Server** ("Go Live"), ou rode na pasta:

```
python3 -m http.server 8000
```

e acesse http://localhost:8000

## Publicar no GitHub Pages (hospedagem provisória)

Pelo VS Code, sem terminal:

1. Abra esta pasta no VS Code.
2. No painel **Source Control**, clique em **Publish to GitHub** e escolha repositório **público**.
3. No GitHub, abra o repositório e vá em **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
5. Em um ou dois minutos o site fica em `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

Pelo terminal, com o GitHub CLI (`gh`) instalado e logado:

```
git init -b main
git add .
git commit -m "Site Dra. Talita Pascoal"
gh repo create talita-pascoal-site --public --source=. --push
gh api -X POST repos/{owner}/talita-pascoal-site/pages -f "source[branch]=main" -f "source[path]=/"
```

## O que ainda falta de conteúdo

- Fotos de exercícios e de atendimentos (galeria)
- Depoimentos de pacientes
- Confirmar se o botão de contato deve abrir o WhatsApp em vez de ligar
