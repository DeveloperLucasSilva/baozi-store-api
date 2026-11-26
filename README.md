# baozi-store-api

# 🥟 API REST - Baozi Store

API REST desenvolvida em **Java com Spring Boot** como atividade prática da disciplina de **Desenvolvimento Web Back-End** do curso de Análise e Desenvolvimento de Sistemas (UNINTER).

O projeto simula o sistema de controle básico da **Baozi Store**, uma pequena loja especializada na venda de pãozinho chinês, permitindo o gerenciamento de **clientes**, **produtos** e **pedidos**.

---

## 🚀 Tecnologias Utilizadas

* **Java 21**
* **Spring Boot** (Spring Web e Spring Data JPA)
* **Banco de Dados H2** (persistência em arquivo local)
* **Maven**
* **Postman** (testes de endpoints)

---

## 📁 Estrutura do Projeto

O projeto segue a arquitetura MVC do Spring, organizado nos pacotes:
* `model` – Entidades JPA (`Cliente`, `Produto`, `Pedido`)
* `repository` – Interfaces de acesso ao banco com `JpaRepository`
* `controller` – Controladores REST com os endpoints CRUD

---

## 📦 Entidades e Campos

* **Cliente:** `id` (`Long`), `nome` (`String`), `clienteDesde` (`LocalDate`)
* **Produto:** `id` (`Long`), `nome` (`String`), `preco` (`BigDecimal`), `estoque` (`Boolean`)
* **Pedido:** `id` (`Long`), `clienteId` (`Long`), `produtoId` (`Long`), `quantidade` (`Integer`)

---

## 🔗 Endpoints da API

| Entidade | Método | Rota | Descrição |
| :--- | :--- | :--- | :--- |
| **Cliente** | `POST` | `/clientes` | Cadastrar novo cliente |
| **Cliente** | `GET` | `/clientes` | Listar todos os clientes |
| **Cliente** | `GET` | `/clientes/{id}` | Consultar cliente por ID |
| **Cliente** | `DELETE` | `/clientes/{id}` | Remover cliente por ID |
| **Produto** | `POST` | `/produtos` | Cadastrar novo produto |
| **Produto** | `GET` | `/produtos` | Listar todos os produtos |
| **Produto** | `GET` | `/produtos/{id}` | Consultar produto por ID |
| **Produto** | `DELETE` | `/produtos/{id}` | Remover produto por ID |
| **Pedido** | `POST` | `/pedidos` | Registrar novo pedido |
| **Pedido** | `GET` | `/pedidos` | Listar todos os pedidos |
| **Pedido** | `GET` | `/pedidos/{id}` | Consultar pedido por ID |
| **Pedido** | `DELETE` | `/pedidos/{id}` | Remover pedido por ID |

---

## ▶️ Como Executar o Projeto

1. Clone o repositório:
   ```bash
    git clone https://github.com/DeveloperLucasSilva/baozi-store-api.git
    ```
2. Abra a pasta do projeto na sua IDE (VS Code, IntelliJ ou Eclipse).

3. Execute a classe principal BaozistoreApplication.java (ou rode ./mvnw spring-boot:run no terminal).

4. A API ficará disponível em http://localhost:8080.

5. O console do banco H2 pode ser acessado em http://localhost:8080/h2-console.

👤 Autor
## Lucas da Silva – RU: 5285091
