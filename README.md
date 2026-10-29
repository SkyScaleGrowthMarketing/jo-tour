# Landing Page — Jo Tour (Visto Americano)

Página única: `index.html` + pasta `images/`.

## Como trocar o link dos botões
Abra `index.html`, procure por `CTA_URL` (perto do final do arquivo) e cole o link entre as aspas:
`CTA_URL: "https://seu-link-aqui",`
Todos os 5 botões passam a usar esse link.

## Meta Pixel
Cole o código base do Pixel no lugar do comentário `<!-- META PIXEL ... -->` dentro do `<head>`.

## Pendências (dependem do cliente)
- [ ] Link de destino dos 5 botões de CTA (`CTA_URL` em branco)
- [ ] Código do Meta Pixel
- [ ] Texto de apresentação da responsável pela Jo Tour (bloco "Quem cuida do seu processo")
- [ ] Domínio próprio (opcional — site está no link do GitHub Pages por enquanto)

## Como publicar atualizações
Depois de qualquer alteração, `git add` + `git commit` + `git push` no mesmo repositório. O GitHub Pages atualiza o site no mesmo link em cerca de 1 minuto.

## Rodar localmente
Na pasta do projeto: `python -m http.server 5173` e abrir `http://localhost:5173`.
