> **Funções e Procedimentos Armazenados**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria uma função armazenada no MySQL que recebe o nome e o sobrenome de uma pessoa como parâmetros e retorna o nome completo?

**Resposta 1:**
Para criar uma função armazenada no MySQL que recebe o nome e o sobrenome de uma pessoa como parâmetros e retorna o nome completo, você pode usar o seguinte código SQL:

```sql
CREATE FUNCTION fn_nome_completo(nome VARCHAR(50), sobrenome VARCHAR(50))
RETURNS VARCHAR(100)
RETURN CONCAT(nome, ' ', sobrenome);
```

**Pergunta 2:** Como você invocaria (chamaria) a função `fn_nome_completo` para obter o nome completo de uma pessoa com nome "John" e sobrenome "Doe"?

**Resposta 2:**
Para invocar (chamar) a função `fn_nome_completo` e obter o nome completo de uma pessoa com nome "John" e sobrenome "Doe", você pode usar o seguinte código SQL:

```sql
SELECT fn_nome_completo('John', 'Doe') AS 'Nome Completo';
```

**Pergunta 3:** Como você criaria um procedimento armazenado no MySQL que recebe o ID de um livro como parâmetro e exibe o título e o preço desse livro?

**Resposta 3:**
Para criar um procedimento armazenado no MySQL que recebe o ID de um livro como parâmetro e exibe o título e o preço desse livro, você pode usar o seguinte código SQL:

```sql
DELIMITER //
CREATE PROCEDURE ver_Preco_Livro(varLivro INT)
BEGIN
    SELECT Nome_Livro, Preco_Livro
    FROM tbl_Livro
    WHERE ID_Livro = varLivro;
END;
//
DELIMITER ;
```

**Pergunta 4:** Como você invocaria (chamaria) o procedimento `ver_Preco_Livro` para obter informações sobre o livro com ID 3?

**Resposta 4:**
Para invocar (chamar) o procedimento `ver_Preco_Livro` e obter informações sobre o livro com ID 3, você pode usar o seguinte código SQL:

```sql
CALL ver_Preco_Livro(3);
```

**Pergunta 5:** Como você excluiria a função `fn_nome_completo` criada na Pergunta 1?

**Resposta 5:**
Para excluir a função `fn_nome_completo` criada na Pergunta 1, você pode usar o seguinte código SQL:

```sql
DROP FUNCTION fn_nome_completo;
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>