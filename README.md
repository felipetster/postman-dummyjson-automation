# DummyJSON API Automation

Projeto de automação de testes de API utilizando Postman e JavaScript (ES6+), com foco na validação de fluxos completos de e-commerce e na integridade de regras de negócio, especialmente financeiras.

O objetivo deste projeto é simular cenários reais de QA, indo além da validação de status HTTP, verificando se o backend se comporta corretamente em cálculos, contratos e regras críticas do negócio.

## Tecnologias Utilizadas
* **Postman** (Client & Runner)
* **JavaScript** (ES6+ Features: Arrow Functions, Reduce, Find, Destructuring)
* **DummyJSON** (API de Testes)

## Cenários Cobertos

### 01. Authentication
* Login com validação de JWT Token
* Persistência de sessão utilizando variáveis de ambiente
* Validação de respostas e estrutura do payload

### 02. Products Management
* Busca de produtos utilizando métodos de Array (`.find`).
* Validação de tipos de dados e performance.
* Cadastro de produtos com dados dinâmicos (Pre-request Script).

### 03. Carts & Checkout (Destaque)
* Auditoria Financeira do Carrinho
* Recalculo do total do carrinho utilizando reduce()
* Validação se o backend soma corretamente os valores
* Verificação item a item:
* Preço unitário x quantidade
* Consistência entre subtotal e total
* Identificação de possíveis falhas de cálculo no servidor.

### 04. User Management (CRUD)
* Criação de usuários com **Faker Data** (Variáveis dinâmicas).
* Testes de Update (PUT) e Deleção Lógica (DELETE).

---

## Evidências de Execução

### 1. Resumo da Execução (Collection Runner)
![Execução com Sucesso](./assets/test-execution-summary.png)

### 2. Auditoria Financeira (Logs)
Validando matemática do servidor via Console:
![Logs do Console](./assets/console-logs.png)

### 3. Código Moderno (Snippet)
Exemplo de uso de `.reduce` e `.find`:
![Código Javascript](./assets/code-snippet-reduce.png)

---

## Como Rodar este Projeto

1.  Clone o repositório.
2.  Importe a Collection e o Environment (pasta `/collections`) no seu Postman.
3.  Selecione o ambiente `DummyJSON Env`.
4.  Execute via **Collection Runner**.

---
*Desenvolvido por Felipe.*
