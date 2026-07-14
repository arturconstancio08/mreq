# Como publicar o app no Vercel e gerar o link

O arquivo `index.html` desta pasta é o app completo (v6) com os 18.585 pedidos embutidos e um código de acesso simples.

**Código de acesso do app: `REI2026`** — a página pede o código na primeira visita. É uma proteção leve, suficiente para uma rodada de feedback, mas não é segurança de verdade (os dados viajam no arquivo). Não divulgue o link publicamente. No app definitivo, com banco de dados e login, isso vira segurança real.

## Caminho recomendado (site em ~5 minutos)

1. Acesse **vercel.com** e crie a conta (pode entrar com sua conta Google — arturconstancio08@gmail.com).
2. Instale o Node.js se ainda não tiver (nodejs.org, versão LTS).
3. Abra o **Prompt de Comando** nesta pasta (`deploy-vercel`) e rode:

```
npx vercel login
npx vercel --prod
```

4. Na primeira vez ele faz 2-3 perguntas — pode aceitar tudo com Enter (nome do projeto: `requisicoes-rei` ou o que preferir).
5. Ao final ele imprime o link, algo como `https://requisicoes-rei.vercel.app` — é esse que você envia para a pessoa, junto com o código REI2026.

## Alternativa sem instalar nada

Se preferir não usar o terminal: **app.netlify.com/drop** — arraste a pasta `deploy-vercel` para a página e o link sai na hora (conta gratuita, mesmo resultado).

## Para atualizar o site depois

Quando eu gerar uma nova versão do app, substituo o `index.html` desta pasta — aí é só rodar `npx vercel --prod` de novo (ou arrastar de novo no Netlify) que o link continua o mesmo, atualizado.

## O que este link NÃO faz ainda

Pedidos cadastrados por quem visitar ficam só no navegador da pessoa (não são compartilhados). Isso é proposital nesta fase: o objetivo é colher opiniões sobre telas e funcionamento. O cadastro compartilhado vem na próxima fase, com banco de dados (Supabase) e login — precisa de ~10 minutos seus para criar a conta, e eu preparo todo o resto.
