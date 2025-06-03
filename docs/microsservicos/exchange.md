# Exchange Service

## Função

Responsável por retornar a taxa de câmbio entre duas moedas, consumindo a API pública da AwesomeAPI e associando a solicitação a um `id-account` extraído do cabeçalho da requisição.

---

## Endpoints

- `GET /exchange/{currency1}/{currency2}` – Retorna as cotações de compra (`buy`) e venda (`sell`), a data/hora atual e o `id-account` informado no header.

### Exemplo de Request

```http
GET /exchange/USD/BRL HTTP/1.1
Host: exchange:8000
id-account: <uuid>
```

### Exemplo de Response

```json
{
  "sell": "5.1234",
  "buy": "5.0987",
  "date": "2025-06-04T14:23:45.123456",
  "id-account": "<uuid>"
}
```

---

## Tecnologias

- FastAPI – framework web para criar endpoints REST.
- requests – biblioteca para chamadas HTTP à API externa.
- Python datetime – para obter timestamp da resposta.

---

## Estrutura de código

- `main.py` – define o endpoint `/exchange/{currency1}/{currency2}` e a lógica de consumo da API externa..
- `requirements.txt` – lista de dependências do projeto

---

## Repositório

[Ver repositório do Exchange Service](https://github.com/Insper-Plataforma/exchange-service)
