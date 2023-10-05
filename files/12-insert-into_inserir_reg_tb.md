> **INSERT INTO - Inserir Dados em Tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



1. **Como você inseriria um novo autor com o nome "João Silva" e sobrenome "Pereira" na tabela `tbl_autores`? O ID_Autor é um campo auto incremento.**

```sql
INSERT INTO tbl_autores (Nome_Autor, Sobrenome_Autor)
VALUES ('João', 'Silva Pereira');
```

2. **Suponha que você tenha uma lista de novos livros em um arquivo CSV chamado `novos_livros.csv` e deseje importá-los para a tabela `tbl_livro`. Como você faria isso usando o MySQL?**

Resposta: Você pode usar o comando LOAD DATA INFILE para importar dados de um arquivo CSV para a tabela. Por exemplo:

```sql
LOAD DATA INFILE 'novos_livros.csv'
INTO TABLE tbl_livro
FIELDS TERMINATED BY ',' ENCLOSED BY '"'
LINES TERMINATED BY '\n'
(Nome_Livro, ISBN13, ISBN10, Data_Pub, Preco_Livro, Id_Categoria, ID_Autor, ID_Editora);
```

3. **Como você inseriria um novo livro com o nome "Python for Data Science" na tabela `tbl_livro`, onde a categoria é "Data Science", o autor é "John Smith" e a editora é "O'Reilly"?**

```sql
-- Primeiro, obtenha os IDs da categoria, autor e editora
SET @categoria_id = (SELECT ID_Categoria FROM tbl_categorias WHERE Categoria = 'Data Science');
SET @autor_id = (SELECT ID_Autor FROM tbl_autores WHERE Nome_Autor = 'John' AND Sobrenome_Autor = 'Smith');
SET @editora_id = (SELECT ID_Editora FROM tbl_editoras WHERE Nome_Editora = 'O''Reilly');

-- Em seguida, insira o novo livro
INSERT INTO tbl_livro (Nome_Livro, ID_Categoria, ID_Autor, ID_Editora)
VALUES ('Python for Data Science', @categoria_id, @autor_id, @editora_id);
```

4. **Suponha que você deseja inserir várias categorias novas na tabela `tbl_categorias`. Como você faria isso em uma única consulta SQL?**

Resposta: Você pode usar a seguinte consulta SQL para inserir várias categorias de uma só vez:

```sql
INSERT INTO tbl_categorias (Categoria)
VALUES
('Machine Learning'),
('Data Visualization'),
('Natural Language Processing');
```

5. **Como você lidaria com erros de inserção ao usar o comando INSERT INTO? Por exemplo, o que acontece se você tentar inserir um livro com um autor que não existe na tabela `tbl_autores`?**

Resposta: O MySQL geralmente lançará um erro de chave estrangeira se você tentar inserir um registro que faz referência a um valor inexistente em uma tabela referenciada. Para evitar isso, é importante garantir que os valores nas colunas estrangeiras correspondam aos valores nas tabelas de referência. Certifique-se de que os autores, categorias e editoras existam antes de tentar inserir registros que os referenciam.

Espero que essas perguntas práticas e avançadas ajudem você a compreender melhor como inserir dados em tabelas MySQL usando o comando INSERT INTO.


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>