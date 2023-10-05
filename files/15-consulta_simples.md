> **SELECT - Consultar Tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



1. **Como você consultaria todos os dados da tabela "clientes" usando o comando SELECT no MySQL?**

   ```sql
   SELECT * FROM clientes;
   ```

2. **Qual é a diferença entre as consultas SQL abaixo?**

   a) `SELECT Nome_Produto FROM produtos WHERE Preco > 50;`

   b) `SELECT Nome_Produto FROM produtos WHERE Preco < 50;`

   Resposta: A consulta (a) retorna o nome dos produtos cujo preço é maior que 50, enquanto a consulta (b) retorna o nome dos produtos cujo preço é menor que 50.

3. **Como você consultaria o nome do autor e o título do livro de todos os livros escritos por um autor específico, por exemplo, o autor com ID 123?**

   ```sql
   SELECT tbl_autores.Nome_Autor, tbl_livro.Nome_Livro
   FROM tbl_livro
   INNER JOIN tbl_autores ON tbl_livro.ID_Autor = tbl_autores.ID_Autor
   WHERE tbl_autores.ID_Autor = 123;
   ```

4. **Como você consultaria o número total de registros na tabela "pedidos"?**

   ```sql
   SELECT COUNT(*) AS TotalPedidos FROM pedidos;
   ```

5. **Como você consultaria a média de preços de todos os produtos na tabela "produtos"?**

   ```sql
   SELECT AVG(Preco) AS MediaPrecos FROM produtos;
   ```

6. **Como você consultaria os nomes dos clientes que fizeram pelo menos um pedido na tabela "clientes"?**

   ```sql
   SELECT DISTINCT clientes.Nome FROM clientes
   INNER JOIN pedidos ON clientes.ID = pedidos.ID_Cliente;
   ```

7. **Como você consultaria os nomes dos autores que não têm livros na tabela "autores" (ou seja, autores não associados a nenhum livro)?**

   ```sql
   SELECT tbl_autores.Nome_Autor FROM tbl_autores
   LEFT JOIN tbl_livro ON tbl_autores.ID_Autor = tbl_livro.ID_Autor
   WHERE tbl_livro.ID_Autor IS NULL;
   ```

8. **Como você consultaria os cinco produtos mais caros na tabela "produtos"?**

   ```sql
   SELECT Nome_Produto, Preco
   FROM produtos
   ORDER BY Preco DESC
   LIMIT 5;
   ```

&nbsp;
  

<div align="center">
   
[Retornar ao índice](/README.md)

</div>