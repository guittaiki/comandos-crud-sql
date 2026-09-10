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
SELECT * FROM usuarios,
WHERE tipo_usuario = 'admin';
```