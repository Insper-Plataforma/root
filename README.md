# Microsserviços - Root Exemplo

Este repositório representa a **estrutura raiz (root)** do projeto, centralizando tudo o que foi necessário para o setup, integração e documentação dos microsserviços desenvolvidos.

---

## Sobre o projeto

Este projeto é um **exemplo completo de arquitetura de microsserviços**, com foco em:

- Integração entre serviços via REST (Spring Cloud OpenFeign)
- Segurança via autenticação JWT
- Monitoramento com Prometheus e Grafana
- Caching com Redis
- Deploy local com Docker Compose
- Integração contínua com Jenkins
- Orquestração com Minikube (Kubernetes local)

---

## Microsserviços incluídos

| Serviço           | Descrição                                               |
| ----------------- | ------------------------------------------------------- |
| `auth-service`    | Responsável por autenticar usuários e emitir tokens JWT |
| `account-service` | Gerencia contas de usuário (cadastro, login etc.)       |
| `product-service` | CRUD de produtos, com suporte a cache Redis             |
| `order-service`   | Criação e consulta de pedidos                           |
| `exchange-service`| Retorna a taxa de câmbio entre duas moedas              |
| `gateway-service` | API Gateway que filtra e redireciona requisições        |

---

## Sobre este repositório (root)

Este repositório **não contém código fonte dos serviços diretamente**. Ele serve como:

- Hub de documentação técnica com MkDocs
- Central de links para cada repositório
- Armazenamento de imagens, configurações e exemplos
- Setup geral para testes locais (Prometheus, Redis, Grafana etc.)

---

## Documentação técnica (MkDocs)

A documentação completa pode ser acessada via site gerado com [MkDocs](https://www.mkdocs.org/), disponível em:

[Documentação do Projeto (Hosted)](https://insper-plataforma.github.io/root)

### Inclui:

- Página para cada microsserviço com explicações técnicas e funcionais
- Fluxo completo das requisições na arquitetura
- Jenkinsfile e pipelines usados nos serviços
- Como foi feito o deploy local com Minikube
- Bottlenecks implementados (Caching + Observabilidade) -> somente no `product-service` para fins de teste, mas facilmente replicável nos outros.
- Referência a todos os repositórios envolvidos

---

## Setup base rodado neste projeto

Este repositório contém os arquivos de configuração base necessários para:

- Subir Redis, Prometheus, Grafana com Docker Compose
- Criar dashboards simples no Grafana para análise
- Monitorar os serviços via `/actuator/prometheus`
- Executar pipelines via Jenkinsfile em cada repositório

---

## Repositórios dos microsserviços

- [Auth](https://github.com/Insper-Plataforma/auth)
- [Account](https://github.com/Insper-Plataforma/account)
- [Product](https://github.com/Insper-Plataforma/product)
- [Order](https://github.com/Insper-Plataforma/order)
- [Auth Service](https://github.com/Insper-Plataforma/auth-service)
- [Account Service](https://github.com/Insper-Plataforma/account-service)
- [Product Service](https://github.com/Insper-Plataforma/product-service)
- [Order Service](https://github.com/Insper-Plataforma/order-service)
- [Exchange Service](https://github.com/Insper-Plataforma/exchange-service)
- [Gateway Service](https://github.com/Insper-Plataforma/gateway-service)

---

## Autor

Ana Helena Caiafa.

Projeto criado para fins educacionais e demonstrativos com foco em arquitetura moderna, automação e documentação de microsserviços.
