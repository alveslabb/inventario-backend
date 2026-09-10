# Backend RESTful de Controle de Inventário

## Descrição

Este projeto foi desenvolvido para realizar o controle de inventário de patrimônio de uma empresa.

O sistema permite cadastrar, consultar, atualizar e excluir itens do inventário.

Os dados são armazenados em um arquivo JSON, simulando um banco de dados.

## Tecnologias utilizadas

- Node.js
- Express
- JavaScript
- JSON
- API REST
- HTTP

## Instalação

Primeiramente, abra a pasta do projeto no Visual Studio Code.

Depois, abra o terminal e execute:

npm install

## Execução

Para iniciar o servidor:

npm start

O servidor será executado em:

http://localhost:3000

## Estrutura

inventario-backend/

data/
- inventario.json

src/
- controllers/
  - inventarioController.js
- routes/
  - inventarioRoutes.js
- services/
  - inventarioService.js

package.json
server.js
README.md

## Rotas

### Criar item

POST /inventario

Exemplo:

{
    "item": "Notebook Dell",
    "local": "Laboratório 01",
    "dataRegistro": "2026-09-10",
    "valor": 3500,
    "patrimonio": "PAT-00125"
}

### Listar itens

GET /inventario

### Buscar item por ID

GET /inventario/1

### Atualizar item

PUT /inventario/1

Exemplo:

{
    "item": "Notebook Dell Atualizado",
    "local": "Laboratório 02",
    "dataRegistro": "2026-09-10",
    "valor": 3700,
    "patrimonio": "PAT-00125"
}

### Excluir item

DELETE /inventario/1

## Funcionalidades adicionais

### Buscar pelo nome

GET /inventario/buscar/nome?nome=Notebook

### Filtrar pelo local

GET /inventario/filtrar/local?local=Laboratório

### Filtrar por valor

GET /inventario/filtrar/valor?valor=3000

Essa rota retorna os itens que possuem valor superior ao informado.

### Verificar patrimônio

GET /inventario/patrimonio/PAT-00125

### Valor total

GET /inventario/total/valor

## Códigos HTTP

200 - Operação realizada com sucesso.

201 - Item criado com sucesso.

400 - Dados inválidos.

404 - Item não encontrado.

409 - Patrimônio já cadastrado.

## Testes

Os testes podem ser realizados utilizando o Postman ou Insomnia.

Testar as seguintes operações:

1. GET /inventario
2. GET /inventario/1
3. POST /inventario
4. GET /inventario
5. PUT /inventario/1
6. GET /inventario/1
7. DELETE /inventario/1
8. GET /inventario
9. Buscar item pelo nome
10. Filtrar item pelo local
11. Filtrar por valor
12. Verificar patrimônio
13. Consultar valor total
![(print01)](./imagens/Captura%20de%20tela%202026-09-03%20164218.png)
![(print02)](./imagens/Captura%20de%20tela%202026-09-03%20164719.png)
![(print03)](./imagens/Captura%20de%20tela%202026-09-10%20160846.png)
![(print04)](./imagens/Captura%20de%20tela%202026-09-10%20160940.png)
![(print05)](./imagens/Captura%20de%20tela%202026-09-10%20160952.png)
![(print06)](./imagens/Captura%20de%20tela%202026-09-10%20161247.png)
![(print07)](./imagens/Captura%20de%20tela%202026-09-10%20161341.png)
![(print08)](./imagens/Captura%20de%20tela%202026-09-10%20161422.png)
![(print09)](./imagens/Captura%20de%20tela%202026-09-10%20161500.png)
![(print10)](./imagens/Captura%20de%20tela%202026-09-10%20161605.png)
![(print11)](./imagens/Captura%20de%20tela%202026-09-10%20161655.png)
![(print12)](./imagens/Captura%20de%20tela%202026-09-10%20161742.png)
![(print13)](./imagens/Captura%20de%20tela%202026-09-10%20161855.png)
![(print14)](./imagens/Captura%20de%20tela%202026-09-10%20161914.png)
![(print15)](./imagens/Captura%20de%20tela%202026-09-10%20161959.png)"# inventario-backend"  
