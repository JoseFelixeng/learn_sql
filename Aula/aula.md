# Introdução ao SQL 

Um banco de dados é apenas um software/ferramenta usada para armazenar uma grande quantidade de dados.

```sql 
SELECT * FROM users;
``` 

O comando acima é usado para selecionar a tabela users.

![alt text](./img/1.png)

A operação `SELECT` no sql é uma das mais comuns pois é um comando usado para a leitura de dados, um exemplo possível é acessar os dados da coluna `id` pertencente a tabela usuario 

```sql 
SELECT id from users;
```

"Obs: O SQL não diferencia letra maiuscula de minuscula."

É possível também fazer uma requisição de mais de um retorno a uma tabela sql da mesma forma feita anteriormente dividindo as colunas por virgula `,`.

```sql

SELECT id, name FROM users; 

```

E por fim podemos recuperar todas as tabelas de uma vez usano o `*`.

```sql

SELECT * FROM users;

```

#### EXEMPLO

Uma empresa possui uma tabela com varias informações, o HR solicita que sejam encontrados os dados dos usuarios que são eles `name` e `balance`, use a linguagem sql para automatizar a buscar.

![alt text](./img/2.png)

**RESOLUÇÂO**

Podemos usar o seguinte comando `SELECT` para ter a leitura da tabela users

```sql

SELECT name, balance FROM users;

```
