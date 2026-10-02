# Fulcro Agência: portfólio

Site estático, sem build. Endereço oficial: https://fulcroagencia.vercel.app/

## Publicar

Publicar = enviar para o GitHub, branch `main` (repositório `Anita270/fulcro-agencia`).
A Vercel está ligada ao repositório e atualiza o site sozinha a cada push.
O GitHub Pages foi desativado; não reativar, para não haver dois endereços do mesmo site.

```
git add -A
git commit -m "..."
git push origin main
```

Depois do push, conferir no endereço oficial se a mudança entrou.

## Publicar um site novo

Padrão para qualquer site novo (de cliente ou conceito), cada um na sua pasta em `C:\Users\User\Projetos`:

1. Criar o repositório no GitHub e enviar o código: `gh repo create <nome> --public --source . --remote origin --push` (conta `Anita270`).
2. Publicar na Vercel pela CLI, dentro da pasta do site: `vercel --prod --yes`.
3. Devolver para a Anita o link curto de produção (`https://<nome>.vercel.app`), não o endereço longo de cada deploy, depois de conferir que ele abre.

A Vercel CLI está instalada globalmente (`npm i -g vercel`). Se `vercel whoami` falhar, o login é com `vercel login`, feito pela Anita.

## Estrutura

- `index.html`: o portfólio inteiro (HTML, CSS e JS num arquivo só). O bloco "CONFIGURAÇÃO" no início do script tem WhatsApp, logo e a lista de projetos.
- `logo.png`: logo recortada rente ao anel, a partir de `Área de Trabalho\Materias Agência\LOGO.png`.
- `prints/`: imagens dos projetos usadas no carrossel e nos cards.
- `sites/<projeto>/index.html`: cópias publicadas dos três sites conceito. Os originais ficam em `C:\Users\User\Projetos\<projeto>\index.html`; ao editar um original, copiar de novo para `sites/` antes de publicar.
- `instagram/`: slides e legendas dos posts. Fica fora do repositório (`.gitignore`). `node gerar.mjs` regera os PNGs.

## Combinados

- Os três sites são projetos conceito: cada um mantém a faixa de aviso no topo, e os botões de WhatsApp apontam para o número da Fulcro, (55) 98453-5365.
- O portfólio não mostra valores de hospedagem; eles são passados na conversa com o cliente.
- Conferir no computador e no celular antes de publicar.
