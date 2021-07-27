<h1 align="center">
  Ig.News blog!
</h1>

<p align="center">
  <a href="#-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-como-executar">Como executar</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-licença">Licença</a>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/static/v1?label=license&message=MIT&color=8257E5&labelColor=000000">
</p>

<br>

## ✨ Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- [React](https://reactjs.org)
- [NextJs](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Sass](https://sass-lang.com/)
- [FaunaDB](https://fauna.com/)
- [Stripe](https://stripe.com/)
- [Prismic CMS](https://prismic.io/)

## 💻 Projeto

Ignews é um blog por assinatura, onde os assinantes poderão visualizar posts de react. Para visualizar os posts é necessário realizar login via GitHub e para assinar, é necessário realizar assinatura. Para controle dos posts é utilizado o Prismic CMS e para gestão dos pagamentos é utilizado o Stripe.

**Para testar a compra com algum cartão, utilize o cartão 4242 4242 4242 4242.

## 🚀 Como executar

- Clone o repositório
- Instale as dependências com `yarn install`
- Inicie a build de páginas estáticas do next com `yarn build`
- Inicie a aplicação com `yarn dev`

## 🚀 Como executar os webhooks do Stripe (Windows)
Para testes em desenvolvimento, o Stripe conta com um webhook que pode ser rodado localmente.

- Dentro de utils/stripe existe um stripe.exe. Abra o mesmo pelo cmd.
- Dentro do CMD: stripe login
- Após login: dentro do CMD: stripe listen --forward-to localhost:3000/api/webhooks
- Não esquecer de copiar o webhook secret em STRIPE_WEBHOOK_SECRET em env.local


Agora você pode acessar [`localhost:3000`](http://localhost:3000) do seu navegador.

## 🚀 Você também precisará criar o arquivo .env.local com as tags abaixo:
```# stripe
STRIPE_API_KEY=xxxxx
NEXT_PUBLIC_STRIPE_PUBLIC_KEY=xxxxx
STRIPE_WEBHOOK_SECRET=xxxxx
STRIPE_SUCCESS_URL=xxxxx
STRIPE_CANCEL_URL=xxxxx

# github
GITHUB_CLIENT_ID=xxxxx
GITHUB_CLIENT_SECRET=xxxxx

# faunaDB
FAUNADB_KEY=xxxxx

# prismic CMS
PRISMIC_ENDPOINT=xxxxx
PRISMIC_ACCESS_TOKEN=xxxxx```

## 📄 Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.
