# SQL SELECT - Exemplos de consultas ao banco Fly By Night

O comando 'SELECT' e usado para **consultar dados armazenados nas tabelas do
banco de dados**.

## SELECT básico

Consultar todos os dados de uma tabela: 

```sql
SELECT * FROM produtos;
```

## SELECT para apenas determinadas colunas

```sql
SELECT nome, preco FROM produtos;
```

## Alterando o nome de exibição das colunas

Usamos o commando 'AS' para criar um **Apelido (alias)**

```sql
SELECT
    nome AS produto,
    preco AS valor, 
FROM produtos;
```    

## Filtrando registros com WHERE

O 'WHERE' permite determinar **quais registros devem
aparecer** no resultado. Na prática, são condições para
execução do 'SELECT'.

### Comparação de igualdade

```sql
SELECT * FROM produtos WHERE quantidade = 0;
```

## Comparação de maior/menor

```sql
SELECT nome, preco FROM produtos WHERE preco > 1000;
```

### Comparação de menor/igual

```sql
SELECT nome, preco FROM produtos WHERE preco <= 1000;
```

### Comparação de diferença

```sql
SELECT * FROM produtos WHERE fornecedor_id <> 1;
```

## Combinando condições

Usamos o `WHERE' e operadores logicos e relacionais.

### Operador AND (E)

Exibir os produtos que custem menos de 500 e quantidade
acima de

```sql
SELECT nome, preco, quantidade FROM produtos
WHERE preco < 500 AND quantidade > 20;
```

### Operador OR (OU)

Exibir os produtos que custem mais de 3000 ou com
quantidade zerada.

```sql
SELECT nome, preco, quantidade FROM
WHERE preco > 3000 OR quantidade = 0;
```

### Operador NOT (NÃO)

Exibir os produtos que **não possuem preço acima de
1000**.

```sql
SELECT nome, preco FROM produtos WHERE NOT preco > 1000;
SELECT nome, preco FROM produtos WHERE preco <= 1000;
```

** Obs .:** o uso do 'NOT' não é obrigatório, desde que
você consiga o mesmo resultado usando uma lógica
diferente, como no exemplo:
`SELECT nome, preco FROM produtos WHERE preco <= 1000;`

### BETWEEN

Exibir produtos com preço ** entre 100 e 500 **.

```sql
SELECT nome, preco FROM produtos
WHERE preco BETWEEN 100 AND 500;
```

### IN

Exibir produtos que tenha o fornecedor ID 1, 4 ou 8.

```sql
SELECT * FROM produtos
WHERE fornecedor_id IN (1, 4, 8);
```

Sem usar o IN', teriamos que fazer a logica com
múltimplos OR':

```sql
SELECT * FROM produtos
WHERE
fornecedor_id = 1 OR
fornecedor_id = 4 OR
fornecedor_id = 8;
```