# Site de serviços

Três páginas estáticas: `index.html` (início), `servicos.html` (detalhe dos serviços) e
`contato.html` (formulário + aviso de privacidade).

## Antes de publicar

Troque os marcadores em todas as páginas: `[NOME]`, `[cidade]`, `[CNPJ]` e `[email]`.

## Formulário

O site é estático: não há servidor para receber o POST. Em `contato.html`, a constante
`ENDPOINT` está `null` e nesse estado o formulário avisa que o envio online não está ligado
e orienta a escrever por e-mail. Ao ligar o backend (Google Apps Script, Formspree,
Cloudflare Worker), coloque a URL do endpoint em `ENDPOINT`.

## Rodar localmente

```bash
python3 serve.py     # http://127.0.0.1:8080 — inclui o POST /api/lead para testar o formulário
```

## Publicação

GitHub Pages a partir da branch `main`. `dados/` e `serve.py` não vão para o repositório
(vide `.gitignore`) — lista de contatos nunca vai para repositório público.
