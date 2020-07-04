<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Desafio 05: Primeiro projeto Node.js
</h3>

<blockquote align="center">“Para quem fica melhor a cada dia, ficar pronto é utopia”!</blockquote>

<p align="center">
  <a href="https://valdirmendes.dev">
    <img alt="Made by Valdir Mendes" src="https://img.shields.io/badge/made%20by-Valdir%20Mendes-%2304D361">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <a href="https://github.com/valdirmendesdev/gostack-fundamentos-nodejs/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/valdirmendesdev/gostack-fundamentos-nodejs?style=social">
  </a>
</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

Nesse desafio, foi proposto que criássemos uma aplicação para treinarmos os conceitos do Node.js junto ao TypeScript, utilizando o conceito de models, repositories e services! (Arquitetura DDD)

## Objetivo da aplicação

Uma aplicação para armazenar transações financeiras de entrada e saída, que deve permitir o cadastro e a listagem dessas transações.

### Rotas da aplicação

Aplicação construída tem as seguintes rotas:

- **`POST /transactions`**: A rota recebe `title`, `value` e `type` dentro do corpo da requisição, sendo `type` o tipo da transação, que deve ser `income` para entradas (depósitos) e `outcome` para saídas (retiradas). O `value` deve possuir um valor numérico. Depois que a transação for cadastrada, o usuário receberá como resposta um objeto conforme o modelo abaixo:

```json
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}
```

- **`GET /transactions`**: Essa rota retorna uma listagem com todas as transações que você cadastrou até agora, junto com o valor de soma de entradas, retiradas e total de crédito. Essa rota retornará um objeto conforme o formato a seguir:

```json
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salário",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freela",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Pagamento da fatura",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Cadeira Gamer",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```

## :running: Rodando a aplicação

Para executar a aplicação, clone este repositório, entre na pasta do projeto e instale as dependências com o seguinte comando no terminal:

```bash
yarn
```

Para rodar a aplicação, execute o seguinte comando no terminal:

```bash
yarn dev:server
```

Para rodar os testes automatizados, execute o seguinte comando no terminal:

```bash
yarn test
```

Neste projeto estamos utilizando o TypeScript então é possível gerar o build do projeto para distribuição. Para isso, rode o seguinte comando:

```bash
yarn build
```

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
