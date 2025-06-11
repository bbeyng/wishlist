=================================================
  Projeto Wishlist - Teste Backend LuizaLabs
=================================================

Este projeto consiste em uma API REST para gerenciar a funcionalidade de "Wishlist" (Lista de Desejos) de um cliente, conforme especificado no teste de backend do LuizaLabs.

A aplicação foi desenvolvida seguindo os princípios da **Clean Architecture**, o que garante um código desacoplado, testável, manutenível e escalável.

---
### Arquitetura do Projeto

O código é organizado em três camadas principais, seguindo a Regra da Dependência (dependências apontam apenas para dentro):

1.  **Domain:** A camada mais interna. Contém as entidades de negócio (`Wishlist`) e as regras de negócio mais puras (ex: limite de 20 produtos). Não depende de nenhum framework ou tecnologia externa.

2.  **Application:** Contém os casos de uso específicos da aplicação (ex: `AddProductToWishlistUseCase`). Orquestra o fluxo de dados e depende apenas da camada de Domínio. Define as "Portas" (interfaces) para a comunicação com o mundo exterior.

3.  **Infrastructure:** A camada mais externa. Contém os detalhes de implementação como a API REST (Spring Web), a conexão com o banco de dados (Spring Data MongoDB) e a configuração. Esta camada "implementa" as portas definidas pela camada de Aplicação.

---
### Funcionalidades Implementadas

A API atende aos seguintes requisitos:
- Adicionar um produto na Wishlist do cliente. 
- Remover um produto da Wishlist do cliente. 
- Consultar todos os produtos da Wishlist do cliente. 
- Consultar se um determinado produto está na Wishlist do cliente.

Regra de Negócio Específica:
- A Wishlist de um cliente deve possuir um limite máximo de 20 produtos. 

---
### Tecnologias Utilizadas

O projeto foi construído utilizando as seguintes tecnologias, conforme as premissas:
- **Linguagem:** Java 17 (compatível com Java 11 ou >) 
- **Framework:** Spring Boot 
- **Gerenciador de Dependências:** Maven 
- **Banco de Dados:** MongoDB (Qualquer NoSQL) 
- **Testes:** JUnit 5 e Mockito
- **Arquitetura:** Clean Architecture, REST 

---
### Pré-requisitos para Execução

Antes de iniciar, garanta que você tenha os seguintes softwares instalados:
1.  JDK 17 ou superior
2.  Apache Maven
3.  MongoDB
4.  Git (opcional, para clonar o projeto)

---
### Como Executar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone <URL_DO_SEU_REPOSITORIO>
   cd wishlist
