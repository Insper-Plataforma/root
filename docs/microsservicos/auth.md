# Auth Service

## Função

Responsável por registrar usuários, autenticar e emitir tokens JWT.

---

## Endpoints

- `POST /auth/register` – Cria usuário
- `POST /auth/login` – Autentica e retorna token
- `POST /auth/solve` – Decodifica token e retorna id da conta

---

## Tecnologias

- Spring Boot
- Feign Client (`AccountController`)
- JWT (`io.jsonwebtoken`)
- CI: Jenkinsfile com `mvn clean package` e Docker build

---

## Estrutura de código

- `AuthService.java` – lógica de autenticação
- `JwtService.java` – geração/validação de token
- `AuthResource.java` – REST Controller

---

## Repositório

[Ver repositório da Interface Auth](https://github.com/Insper-Plataforma/auth)

[Ver repositório do Auth Service](https://github.com/Insper-Plataforma/auth-service)
