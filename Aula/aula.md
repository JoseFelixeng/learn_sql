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

## SQL VS NoSQL 

![alt text](./img/3.png)

O primeiro ponto a ser debatido é que bancos de dados baseados em SQL tendem a ser muito parecidos, já para o NoSQL essas diferenças são gritantes chegando a serem parecidos apenas por usar SQL. Sendo assim os bancos de dados SQL são considerados `general purpose` pois podem ser usados por diversas linguagens diferentes. Já bancos de dados baseados em NoSQL tendem a ser mais expecificos.  


#### Criando uma tabela 

`CREATE TABLE users (id INTEGER, name TEXT, age INTEGER);` é usado para criar uma tabela, com 3 entradas, logo após já inserir os usuarios.

```sql

CREATE TABLE users (id INTEGER, name TEXT, age INTEGER);
INSERT into users (id, name, age) values (1, 'John Doe', 21);
INSERT into users (id, name, age) values (2, 'Montgomery Burns', 33);
SELECT * FROM users;


```

O primeiro passo para criar uma tabela é usar o comando `CREATE TABLE` junto do nome ao qual a tabela irá receber, depois expecificamos as colunas que irão compor a tabela.

```sql 

CREATE TABLE funcionarios (id INTEGER, name TEXT, idade INTEGER, is_manager BOOLEAN, salario FLOAT);

```

Além disso pode ser identada da seguinte forma. 

```sql 

CREATE TABLE employees(
    id INTEGER,
    name TEXT,
    idade INTEGER,
    is_manager BOOLEAN,
    salario FLOAT
);

```

#### EXEMPLO 

Crie uma tabela para uma empresa na qual possa ser inseridos pessoas:

```sql

CREATE TABLE people (
  id INTEGER,
  handle TEXT,
  name TEXT,
  age INTEGER,
  balance INTEGER,
  is_admin BOOLEAN
);

```
Um ponto importante sobre table é que alterar uma tabela em uso pode não ser uma boa pratica pois pode acarretar em oscilações e bugs dentro do BD.

