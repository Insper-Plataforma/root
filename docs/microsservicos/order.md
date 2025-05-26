# Order Service

## Função

Responsável pelo registro e consulta de pedidos realizados por usuários. Cada pedido contém múltiplos produtos com cálculo de total automático.

---

## Endpoints

- `POST /order` – Cria um novo pedido
- `GET /order` – Lista todos os pedidos
- `GET /order/{id}` – Retorna os detalhes de um pedido específico

---

## Tecnologias

- Spring Boot
- Spring Data JPA
- Integração com `product-service` via Feign Client
- Validação do `id-account` via headers (injetado pelo gateway)
- CI: Jenkinsfile com `mvn clean package` e Docker build

---

## Estrutura de código

- `OrderService.java` – lógica de cálculo e persistência de pedidos
- `OrderModel.java` / `OrderItemModel.java` – entidades JPA
- `OrderRepository.java` / `OrderItemRepository.java` – repositórios
- `OrderResource.java` – REST Controller
- `OrderParser.java` – conversão de entrada/saída
- `Order.java` / `OrderItem.java` – entidades de domínio

---

## Repositório

[Ver repositório da Interface Order](https://github.com/Insper-Plataforma/order)

[Ver repositório do Order Service](https://github.com/Insper-Plataforma/order-service)
