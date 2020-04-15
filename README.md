<h2 align="center">
  Desafio 05: Primeiro projeto Node.js
</h2>

## 🚀 Sobre o desafio

O objetivo desse desafio é criar uma aplicação para continuar treinando o que foi aprendendido até agora no Node.js junto ao TypeScript, utilizando o conceito de models, repositories e services!

Essa será uma aplicação para que deve armazenar transações financeiras de entrada e saída, que deve permitir o cadastro e a listagem dessas transações.

### **🖥 Instalação**

```
    /* Clonar o repositório */
    git clone https://github.com/Jonathan-Sales/gostack11-fundamentos-nodejs.git

    /* Instalar as dependências */
    yarn

    /* Iniciar o servidor */
    yarn dev:server
```

- Para rodar os testes, execute o comando abaixo:

```
    yarn test
```

### **Rotas da aplicação**

- **`POST /transactions`**: A rota recebe os parâmetros `title`, `value` e `type` dentro do corpo da requisição, sendo `type` o tipo da transação, que deve ser `income` para entradas (depósitos) e `outcome` para saidas (retiradas). Ao cadastrar uma nova transação, a API retorna os dados salvos no formato abaixo:

```
    {
      "id": "uuid",
      "title": "Salário",
      "value": 3000,
      "type": "income"
    }
```

- **`GET /transactions`**: Essa rota retorna uma listagem com todas as transações que foram cadastradas até o momento, junto com o valor de soma de entradas, retiradas e total de crédito. Essa rota retorna um objeto com o seguinte formato:

```
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

## **📝 Licença**

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](https://github.com/Rocketseat/bootcamp-gostack-desafios/blob/master/desafio-01/LICENSE.md) para mais detalhes.
