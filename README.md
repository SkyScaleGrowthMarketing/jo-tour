# Landing Page — Jo Tour (Visto Americano)

Página única: `index.html` + pasta `images/`.

## Botões de CTA
Os 4 botões da página ("QUERO MEU DIAGNÓSTICO GRATUITO" etc.) abrem um modal com o formulário "FAP 01 Visto" do GoHighLevel (embed `dxhdsjKbdt86gNwEoAOO`), em vez de linkar para uma URL externa. O modal e a lógica de abrir/fechar estão no final do `index.html`, perto do `</footer>`. Para trocar o formulário, troque o `src` do `<iframe>` dentro de `#formModal`.

## Meta Pixel
Cole o código base do Pixel no lugar do comentário `<!-- META PIXEL ... -->` dentro do `<head>`. O clique nos botões já dispara `fbq('track', 'Lead', ...)` quando o Pixel estiver instalado — falta só colar o código base.

## Pendências (dependem do cliente)
- [x] Link de destino dos botões de CTA — resolvido: abre o formulário embutido do GoHighLevel
- [ ] Código base do Meta Pixel
- [ ] Texto de apresentação da responsável pela Jo Tour (bloco "Quem cuida do seu processo")
- [ ] Domínio próprio `jotour.com.br` — `CNAME` já configurado no repositório; falta criar os registros DNS no Registro.br (ver seção "Domínio" abaixo) para o link pendurar
- [ ] Confirmar no GoHighLevel se a confirmação do formulário deve redirecionar para `obrigado.html` do site ou usar a tela de confirmação própria do GHL

## Domínio (jotour.com.br, via Registro.br)
O arquivo `CNAME` na raiz do repositório já diz ao GitHub Pages para servir o site em `jotour.com.br`. Falta criar, no DNS do Registro.br (painel → domínio → DNS), os seguintes registros:

**Para o domínio raiz (`jotour.com.br`) — 4 registros A:**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**Para `www.jotour.com.br` — 1 registro CNAME:**
```
skyscalegrowthmarketing.github.io.
```

Depois de criar os registros, a propagação leva de alguns minutos a algumas horas. Quando propagar, confirmar em Settings → Pages do repositório que o domínio foi verificado e marcar "Enforce HTTPS".

## Como publicar atualizações
Depois de qualquer alteração, `git add` + `git commit` + `git push` no mesmo repositório. O GitHub Pages atualiza o site no mesmo link em cerca de 1 minuto.

## Rodar localmente
Na pasta do projeto: `python -m http.server 5173` e abrir `http://localhost:5173`.
