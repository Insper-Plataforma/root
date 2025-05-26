# Fluxo da Plataforma

## Cenário completo

1. Usuário chama `POST /auth/login` → retorna token
2. Frontend envia esse token em headers para outras rotas
3. O `gateway-service` intercepta, valida com `/auth/solve`, e injeta `id-account` no header
4. As rotas internas (`/order`, `/product`, etc.) recebem o `id-account` e processam normalmente

---

## Exemplo de requisição

```http
GET /order/123
Authorization: Bearer eyJhbGciOiJI...
```

O gateway:

- Valida o token
- Chama `/auth/solve` para verificar o token
- Encaminha `/order/123` com:

```http
id-account: abc123
```

Esse fluxo é garantido pelos filtros globais do `gateway-service`.
