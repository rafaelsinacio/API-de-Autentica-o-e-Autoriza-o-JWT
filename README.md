# API de Autenticação e Autorização JWT

Esta API é uma implementação básica de autenticação e autorização utilizando JWT (JSON Web Tokens) em uma aplicação Spring Boot.

## Funcionalidades

- Login com validação de usuário e senha.
- Emissão de token JWT para autenticação.
- Validação do token JWT.
- Endpoints protegidos por roles (`ADMIN`, `USER`).
- Configuração segura com Spring Security e criptografia de senhas usando BCrypt.
- Inicialização automática de usuários padrão (`admin` e `user`).

## Tecnologias

- Java 17+
- Spring Boot
- Spring Security
- JWT (via Spring Security OAuth2 Resource Server)
- BCrypt para hashing de senhas
- H2 Database (para testes)
- Swagger/OpenAPI para documentação de APIs

## Endpoints principais

| Método | Endpoint        | Descrição                                  |
|--------|-----------------|--------------------------------------------|
| POST   | `/auth/login`   | Realiza login e retorna token JWT.        |
| POST   | `/auth/validate`| Valida um token JWT.                        |
| GET    | `/api/hello`    | Exemplo de endpoint protegido para `USER`.|
| GET    | `/api/admin`    | Endpoint protegido para `ADMIN`.           |

