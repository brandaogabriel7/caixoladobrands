---
{"dg-publish":true,"dg-path":"SQL Injection.md","permalink":"/sql-injection/","title":"SQL Injection","created":"2023-12-05T22:30:00.000-03:00","updated":"2026-01-23T14:24:22.464-03:00"}
---

Injeção SQL (SQL Injection) é uma vulnerabilidade em que uma entrada de usuário pode ser usada de forma maliciosa para alterar a operação executada em um banco de dados.

O que acontece é que, quando a entrada de um usuário é concatenada a uma consulta sem nenhuma validação ou tratamento, ela pode conter código SQL além do dado requerido para a consulta e esse código extra vai ser executado não intencionalmente. Isso expõe a aplicação a riscos como exposição de dados sensíveis, exclusão de dados ou outras operações perigosas.

Um exemplo de injeção SQL é o acréscimo de instruções que façam com que uma condição sempre seja verdadeira, retornando todos os registros de uma tabela ao invés de um específico:
```sql
SELECT username, password FROM users WHERE ID = {userId}
```
Se o `userId` passado contiver o valor `1 OR 1=1`, a query fica assim:
```sql
SELECT username, password FROM users WHERE ID = 1 OR 1=1
```
Essa alteração retornaria os dados de login de todos os usuários ao invés de apenas um, como era a intenção.

Além dessa, existem outras injeções possíveis que permitem inserir instruções para apagar tabelas ou realizar outras ações perigosas.

## Parâmetros SQL para proteção
Uma forma de proteger sua aplicação de ataques de Injeção SQL é a utilização de parâmetros SQL. Parâmetros SQL são uma forma controlada de passar dados para uma query em tempo de execução. Eles garantem que a entrada do usuário será tratada apenas como dados da query e nenhuma instrução maliciosa pode ser injetada.

## Referências e Outras leituras
- [SQL Injection](https://www.w3schools.com/sql/sql_injection.asp)