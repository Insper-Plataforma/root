# Product Service

## Função

Responsável pelo cadastro, consulta e exclusão de produtos. Utiliza cache com Redis para otimização de desempenho e Prometheus + Grafana para observabilidade (configurados apenas nesse microsserviço para fins educativos, mas facilmente replicável nos outros microsserviços).

---

## Endpoints

- `POST /product` – Cria produto
- `GET /product` – Lista todos os produtos
- `GET /product/{id}` – Retorna um produto pelo ID
- `DELETE /product/{id}` – Remove um produto

---

## Tecnologias

- Spring Boot
- Spring Data JPA
- Redis + Spring Cache (`@Cacheable`)
- Prometheus + Grafana
- CI: Jenkinsfile com `mvn clean package` e Docker build

---

## Estrutura de código

- `ProductService.java` – lógica de negócio com cache
- `ProductModel.java` – entidade JPA
- `ProductRepository.java` – repositório de produtos
- `ProductResource.java` – REST Controller
- `ProductParser.java` – conversões entre DTOs e entidade
- `Product.java` – entidade de domínio

---

## Repositório

[Ver repositório da Interface Product](https://github.com/Insper-Plataforma/product)

[Ver repositório do Product Service](https://github.com/Insper-Plataforma/product-service)
