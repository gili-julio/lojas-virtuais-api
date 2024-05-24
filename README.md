## Sumário

- [Visão Geral](#visão-geral)
- [Design do Banco de Dados](#design-do-banco-de-dados)
- [Endpoints da API](#endpoints-da-api)
- [Testes](#testes)
- [Manutenção e Suporte](#manutenção-e-suporte)

## Visão Geral

**Componentes Principais:**
 - Frontend: Aplicativo mobile (Android) desenvolvido em Kotlin ([github-repo](https://github.com/gili-julio/lojas-virtuais-app))
 - Backend: API REST desenvolvida em Java com Spring Boot
 - Banco de Dados: postgreSQL

**Principais Funcionalidades:**
 - Retornar todas as lojas cadastradas
 - Retornar todos os produtos das lojas cadastradas
 - Retornar usuário ao ser solicitado
 - CRUD de stores/itens/users

## Design do Banco de Dados

### Modelo de dados

**Lojas (stores)**
 - `id`: Identificador único da loja
 - `id.user`: Identificador do usuário que cadastrou a loja
 - `name`: Nome da loja
 - `category`: Categoria da loja (Ex: eletronicos, roupas)
 - `createdAt`: Data do cadastro da loja no app
 - `updateAt`: Data da última alteração no cadastro da loja

**Produtos (itens)**
 - `id`: Identificador único do produto
 - `id.store`: Identificador da loja que o produto foi cadastrado
 - `price`: Preço do produto
 - `createdAt`: Data do cadastro do produto no app
 - `updateAt`: Data da última alteração no cadastro do produto

**Usuários (users)**
 - `id`: Identificador único do usuário
 - `name`: Nome completo do usuário
 - `nickname`: Apelido do usuário
 - `passwordHashed`: Senha criptografada do usuário
 - `createdAt`: Data do cadastro do usuário no app
 - `updateAt`: Data da última alteração no cadastro do usuário

## Endpoints da API

### Endpoints

 - Citar os métodos e endpoints da API, exemplo:
 - **(GET) "/lojas":** Retorna todas as lojas
 ```json
 {
  "lojas": ["exemplar", "de novo imoveis"],
  "total": "2"
 }
 ```

## Testes

 - Citar os testes realizados depois

## Manutenção e Suporte

 - Citar como é feita a manutenção
 - Citar por onde entrar em contato para suporte

