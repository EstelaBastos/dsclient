# DSClient 

> Aplicação desenvolvida durante o Bootcamp Spring React da DevSuperior.

## Tecnologias

Esse projeto utiliza [H2](https://www.h2database.com/html/main.html) e [Spring](https://spring.io/projects).

Dependências necessárias para execução do projeto: 

  - JDK 11
  - [Maven 3.8.3](https://maven.apache.org/index.html)

## Como instalar?

O projeto utiliza um repositório para versionamento do backend.

### Backend (Spring)
1. Clone o repositório
```
3. git clone https://github.com/EstelaBastos/dsclient.git
4. cd backend
```
 2. Instale as dependências e execute o projeto
```
3. mvnw clean install
4. mvnw spring-boot:run
```
3. Acesse projeto em http://localhost:8080/

## Operações disponíveis

A aplicação que realiza um CRUD completo de Web Services REST para acessar um recurso de clientes, contendo as seguintes operações de busca paginada, busca por id, inserção, atualização e deleção de clientes.

|Verbo HTTP| Rota  | Descrição |
|--|--|--|
| **GET** | `/clients?page=0&linesPerPage=6&direction=ASC&orderBy=name` |  Busca paginada de clientes|
| **GET** | `/clients/{id}` |  Busca um cliente por id |
| **POST** | `/clients` <br /> <code>{ <br />&nbsp;&nbsp;&nbsp;"name": Nome de Exemplo",<br />&nbsp;&nbsp;&nbsp; "cpf": "12345678901", <br />&nbsp;&nbsp;&nbsp; "income": 6500.0, <br />&nbsp;&nbsp;&nbsp; "birthDate": "1994-07-20T10:30:00Z", <br />&nbsp;&nbsp;&nbsp; "children": 2 <br />}</code>|  Insere um novo cliente |
| **PUT** | `/clients/{id}`  <br /> <code>{ <br />&nbsp;&nbsp;&nbsp;"name": Nome Alterado",<br />&nbsp;&nbsp;&nbsp; "cpf": "12345678901", <br />&nbsp;&nbsp;&nbsp; "income": 6500.0, <br />&nbsp;&nbsp;&nbsp; "birthDate": "1994-07-20T10:30:00Z", <br />&nbsp;&nbsp;&nbsp; "children": 2 <br />}</code> |  Atualiza um cliente por id |
| **DELETE** | `/clients/{id}` |  Deleta um cliente por id |