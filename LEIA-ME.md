# Meu Bolso (versão que guarda no aparelho)

Não precisa de Supabase, login nem configuração. Os lançamentos ficam salvos no próprio navegador do aparelho.

## Publicar no Cloudflare Pages

Se você já tem o repositório do Meu Bolso no GitHub:

1. Apague do repositório os arquivos da versão anterior: `config.js`, `supabase.js`, `591.supabase.js` e `supabase.sql`.
2. Envie estes arquivos para a raiz do repositório, substituindo os que já existem: `index.html`, `sw.js`, `manifest.webmanifest` e `_headers`.
3. Confirme que a pasta `icons` está no repositório, com os 6 arquivos de imagem dentro. Se faltar, arraste a pasta `icons` inteira.
4. O Cloudflare publica sozinho. Depois, abra o endereço `.pages.dev` e recarregue com Ctrl + Shift + R.

Se for criar tudo do zero: crie o repositório, envie todos os arquivos desta pasta na raiz e, no Cloudflare, use **Workers & Pages > Create > Pages > Connect to Git**, com Build command vazio e Build output directory `/`.

## No celular

Abra o endereço no navegador e use **Adicionar à tela inicial**. O ícone é a sua logo.

## Cuidados com os dados

- Cada aparelho (e cada navegador) tem os próprios lançamentos. Celular e computador não se misturam.
- Limpar os dados do navegador apaga tudo. Por isso, na aba **Reserva**, use **Baixar backup** de vez em quando.
- Para levar os dados de um aparelho para outro, baixe o backup em um e use **Restaurar backup** no outro.

## Atualizações

Troque o `index.html` no GitHub e o Cloudflare publica. O app busca a versão nova sempre que abre com internet. Se mudar ícones ou o manifesto, aumente o número da versão no `sw.js`.
