## Consultas básicas

```sql
SELECT * FROM usuarios; 
SELECT nome, email FROM usuarios;
SELECT * FROM categorias;
SELECT titulo, data_publicacao FROM noticias
SELECT
    nome AS "identificação",
    senha AS chave 
FROM usuarios;
```

## Consultas com WHERE 

```sql 
SELECT * FROM usuarios WHERE tipo_usuario = 'admin';
SELECT * FROM noticias WHERE destaque = 'sim'; 
SELECT * FROM noticias WHERE id_categoria = 2;
SELECT * FROM usuarios WHERE tipo_usuario <> 'admin';
```

## Combinando condições

```sql
SELECT * FROM noticias
WHERE destaque = 'sim'
AND id_categoria = 2;

SELECT * FROM usuarios
WHERE tipo_usuario = 'admin'
OR tipo_usuario = 'editor';
```

## Pesquisas com LIKE

```sql
SELECT * FROM noticias
WHERE titulo LIKE '%tecnologia%';

SELECT * FROM noticias
WHERE titulo LIKE '%Inteligência%';
```

## Ordenação

```sql
SELECT * FROM noticias
ORDER BY data_publicacao DESC;

SELECT * FROM usuarios
ORDER BY nome ASC;
```

## Funções de agregação

```sql
SELECT COUNT(*) AS quantidade_Usuarios
FROM usuarios;

SELECT COUNT(*) AS quantidade_Noticias
FROM noticias;

SELECT MIN(data_publicacao) AS noticia_Mais_Antiga,
       MAX(data_publicacao) AS noticia_Mais_Recente
FROM noticias;
```

## Desafio

```sql
SELECT titulo AS titulo_noticia,
       data_publicacao AS data_publicacao
FROM noticias
WHERE titulo LIKE '%a%'
AND destaque = 'sim'
ORDER BY data_publicacao DESC;
```