
# 🏥 estudo_spring - API REST de Clínica Médica

Este repositório contém o projeto desenvolvido durante a formação **Java e Spring Boot** da [Alura](https://www.alura.com.br/), com o objetivo de praticar a criação de uma API REST simulando o backend de uma clínica médica.

## 🚀 Tecnologias Utilizadas

- Java 17
- Spring Boot
- Spring Data JPA
- MySQL 
- Flyway (migrações do banco de dados)
- Maven
- JUnit
- Postman / Swagger (para testes de endpoints)

## 📋 Funcionalidades da API

A aplicação expõe os seguintes endpoints:

### Médicos

- `GET /medicos` - Listagem de médicos
- `POST /medicos` - Cadastro de médico
- `PUT /medicos` - Atualizar médico
- `DELETE /medicos` - Deletar médico
- `GET /medicos/{id}` - Detalhar médico

### Pacientes

- `GET /pacientes` - Listagem de pacientes
- `POST /pacientes` - Cadastro de paciente

### Consultas

- `POST /consultas` - Cadastro de consulta

### Autenticação

- `POST /login` - Efetuar login

## 🗄️ Configuração do Banco de Dados

### Flyway e Scripts de Migração

Os scripts de migração para criação e alteração das tabelas encontram-se em:
```
src/main/resources/db/migration
```
Nessa pasta, estão arquivos como:

- `V1__create-table-medicos.sql`
- `V2__alter-table-medicos-add-column-telefone.sql`
- `V3__alter-table-medicos-change-telefone.sql`
- `V4__create-table-paciente.sql`
- `V5__alter-table-medicos-add-column-ativo.sql`
- `V6__create-table-usuario.sql`
- `V7__create-table-consultas.sql`
- `V8__alter-table-add-column-consulta.sql`
- `V9__alter-table-paciente-add-column-ativo.sql`

Esses scripts estão escritos para **MySQL** (utilizando tipos de dados e sintaxe compatíveis). Ao iniciar a aplicação, o Flyway aplicará automaticamente essas migrações.

## ✅ Testes

O projeto contém classes de testes automatizados para verificar o funcionamento correto dos serviços da API. Estes testes utilizam banco em memória (H2) e cobertura básica dos endpoints.

## 💻 Como rodar o projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/estudo_spring.git
   ```
2. Importe o projeto em sua IDE favorita (recomendo o IntelliJ ou Eclipse).
3. Ajuste as configurações de conexão MySQL no arquivo `application.properties` ou `application.yml`.
4. Execute a aplicação a partir da classe `EstudoSpringApplication`.
5. Acesse a interface do Swagger (se configurada) via:
   ```
   http://localhost:8080/swagger-ui.html
   ```
6. Utilize ferramentas como Postman ou Insomnia para testar os endpoints.

## 📚 Aprendizados

Durante o desenvolvimento deste projeto, foram aplicados conceitos como:

- Criação de APIs RESTful com Spring Boot
- Utilização de DTOs
- Boas práticas com JPA e Hibernate
- Migrações de banco de dados com Flyway em MySQL
- Validações com Bean Validation
- Testes automatizados com JUnit

---

**Projeto com fins educativos.**

Autor: Mayk Suel
