-- CADASTRO DOS USUÁRIOS

```sql
INSERT INTO usuarios (nome, email, senha, tipo) VALUES
('Ana Silva', 'ana@email.com', '123abc', 'editor'),
('Bruno Souza', 'bruno@email.com', 'abc456', 'admin'),
('Carla Mendes', 'carla@email.com', '789xyz', 'editor');
```

-- CADASTRO DAS CATEGORIAS

```sql
INSERT INTO categorias (nome) VALUES
('Tecnologia'),
('Educação'),
('Entretenimento');
```

-- CADASTRO DAS NOTÍCIAS

```sql
INSERT INTO noticias 
(titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria)
VALUES

(
    'Novas tecnologias mudam o dia a dia',
    'Ferramentas digitais estão cada vez mais presentes na rotina das pessoas.',
    'A tecnologia está cada vez mais presente na vida das pessoas. Aplicativos, computadores e outros recursos digitais ajudam em tarefas do trabalho, dos estudos e também do lazer.',
    'tecnologia.jpg',
    'sim',
    1,
    1
),

(
    'Tecnologia na educação ganha espaço',
    'Escolas estão utilizando recursos digitais para melhorar o aprendizado.',
    'O uso da tecnologia nas escolas vem aumentando nos últimos anos. Computadores, celulares e plataformas digitais podem auxiliar professores e alunos durante as atividades e facilitar o acesso a diferentes conteúdos.',
    'educacao.jpg',
    'sim',
    3,
    2
),

(
    'Novidades no mundo do entretenimento',
    'Filmes, séries e jogos continuam conquistando o público.',
    'O setor de entretenimento continua apresentando novidades para o público. Filmes, séries e jogos digitais estão entre as opções mais procuradas por pessoas que buscam diversão em seu tempo livre.',
    'entretenimento.jpg',
    'nao',
    2,
    3
),

(
    'Inteligência artificial é destaque',
    'A inteligência artificial vem sendo utilizada em diferentes áreas.',
    'A inteligência artificial vem sendo utilizada em diferentes áreas, ajudando na realização de tarefas e no processamento de informações. Seu uso tem crescido e gerado novas possibilidades para empresas e usuários.',
    'ia.jpg',
    'sim',
    1,
    1
);
```

## alterar o nome do usuario

```sql
UPDATE usuarios SET nome = 'Frederico' 
WHERE id = 1;
```


## alterar o tipo do usuario

```sql
UPDATE usuarios SET tipo_usuario = 'admin'
WHERE id = 3;
```

## alterar o nome da categoria

```sql
UPDATE categorias SET nome = 'lazer'
WHERE id = 3;
```

## alterar o titulo da noticia

```sql
UPDATE noticias SET titulo = 'Avanço da Tecnologia'
WHERE id = 10;
```

## alterar destaque

```sql
UPDATE noticias SET destaque = 'sim'
WHERE id = 11;
```

## alterar categoria da noticia

```sql
UPDATE noticias SET id_categoria = 2
WHERE id = 12;
```


## delete 

```sql
DELETE FROM noticias WHERE id = 9;
DELETE FROM categorias WHERE id = 3;
DELETE FROM usuarios WHERE id = 1;
```
