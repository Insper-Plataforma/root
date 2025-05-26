# Account Service

## Função

Responsável pela criação, consulta e autenticação de contas de usuários. Também faz a validação de senha via hash SHA-256.

---

## Endpoints

- `POST /account` – Cria uma nova conta
- `GET /account` – Lista todas as contas
- `POST /account/login` – Busca conta pelo email e senha
- `GET /account/whoami` – Retorna informações da conta autenticada

---

## Tecnologias

- Spring Boot
- Spring Data JPA
- Flyway para versionamento do banco
- SHA-256 para hashing de senha
- CI: Jenkinsfile com `mvn clean package` e Docker build

---

## Estrutura de código

- `AccountService.java` – lógica de criação e autenticação
- `AccountModel.java` – entidade JPA
- `AccountRepository.java` – repositório com Spring Data
- `AccountResource.java` – REST Controller
- `Account.java` – entidade de domínio

---

## Repositório

[Ver repositório da Interface Account](https://github.com/Insper-Plataforma/account)

[Ver repositório do Account Service](https://github.com/Insper-Plataforma/account-service)

