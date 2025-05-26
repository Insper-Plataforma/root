# Gateway Service

## Função

O `gateway-service` atua como ponto de entrada central da aplicação. Ele valida tokens, autentica rotas e redireciona requisições para os serviços internos.

---

## Responsabilidades

- Validação de token JWT via `/auth/solve`
- Injeção de `id-account` no header
- Redirecionamento para `product`, `order`, `account` etc.
- CORS liberado para acesso do frontend

---

## Tecnologias

- Spring Cloud Gateway
- Spring WebFlux
- WebClient para comunicação com `auth-service`
- Filtro global (`AuthorizationFilter`) com lógica customizada
- CI: Jenkinsfile com `mvn clean package` e Docker build

---

## Estrutura de código

- `AuthorizationFilter.java` – filtro global para autenticação
- `RouterValidator.java` – define quais rotas são públicas
- `CorsFilter.java` – configuração de CORS
- `GatewayResource.java` – endpoint de sistema `/info`
- `application.yaml` – configura todas as rotas

---

## Repositório

[Ver repositório do Gateway Service](https://github.com/Insper-Plataforma/gateway-service)
