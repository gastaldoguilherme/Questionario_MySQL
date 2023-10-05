> **CREATE TABLE - Criar Tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



**1. Qual é a sintaxe básica para criar uma tabela no MySQL?**

   - Resposta em SQL:
   ```sql
   CREATE TABLE IF NOT EXISTS nome_tabela (
      coluna tipo_dados constraints,
      coluna tipo_dados constraints,
      coluna tipo_dados constraints,
      ...
   );
   ```

**2. Como você cria uma tabela chamada `tbl_livro` com várias colunas, incluindo uma coluna de chave primária autoincrementada?**

   - Resposta em SQL:
   ```sql
   CREATE TABLE IF NOT EXISTS tbl_livro (
      ID_Livro SMALLINT AUTO_INCREMENT PRIMARY KEY,
      Nome_Livro VARCHAR(70) NOT NULL,
      ISBN13 CHAR(13),
      ISBN10 CHAR(10),
      Data_Pub DATE NOT NULL,
      Preco_Livro DECIMAL(6,2) NOT NULL,
      ID_Categoria SMALLINT,
      ID_Autor SMALLINT NOT NULL,
      ID_Editora VARCHAR(70) NOT NULL
   );
   ```

**3. Como você cria uma tabela chamada `tbl_autores` com uma coluna de chave primária?**

   - Resposta em SQL:
   ```sql
   CREATE TABLE IF NOT EXISTS tbl_autores (
      ID_Autor SMALLINT PRIMARY KEY,
      Nome_Autor VARCHAR(50) NOT NULL,
      Sobrenome_Autor VARCHAR(60) NOT NULL
   );
   ```

**4. Como você cria uma tabela chamada `tbl_categorias` com uma coluna de chave primária?**

   - Resposta em SQL:
   ```sql
   CREATE TABLE IF NOT EXISTS tbl_categorias (
      ID_Categoria SMALLINT PRIMARY KEY,
      Categoria VARCHAR(30) NOT NULL
   );
   ```

**5. Como você cria uma tabela chamada `tbl_editoras` com uma coluna de chave primária autoincrementada?**

   - Resposta em SQL:
   ```sql
   CREATE TABLE IF NOT EXISTS tbl_editoras (
      ID_Editora SMALLINT PRIMARY KEY AUTO_INCREMENT,
      Nome_Editora VARCHAR(50) NOT NULL
   );
   ```

Essas perguntas e respostas em código devem ajudar a entender como criar tabelas no MySQL com base na sintaxe fornecida.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>