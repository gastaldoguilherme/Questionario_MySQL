> **SELECT + ORDER BY - Consultas com Ordenação**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


1. **Como você consultaria todos os registros da tabela "produtos" ordenados em ordem alfabética crescente pelo nome do produto?**

   ```sql
   SELECT * FROM produtos
   ORDER BY Nome_Produto ASC;
   ```

2. **Como você consultaria os 10 produtos mais caros da tabela "produtos" ordenados em ordem decrescente de preço?**

   ```sql
   SELECT * FROM produtos
   ORDER BY Preco DESC
   LIMIT 10;
   ```

3. **Como você consultaria os registros da tabela "vendas" ordenados primeiro pelo nome do cliente em ordem alfabética crescente e, em seguida, pela data da venda em ordem decrescente?**

   ```sql
   SELECT * FROM vendas
   ORDER BY Nome_Cliente ASC, Data_Venda DESC;
   ```

4. **Como você consultaria os registros da tabela "pedidos" ordenados pelo ID do produto em ordem crescente e, para produtos com o mesmo ID, em ordem decrescente de quantidade?**

   ```sql
   SELECT * FROM pedidos
   ORDER BY ID_Produto ASC, Quantidade DESC;
   ```

5. **Como você consultaria os registros da tabela "funcionarios" ordenados em ordem alfabética decrescente pelo sobrenome dos funcionários e, em seguida, pelo nome em ordem alfabética crescente?**

   ```sql
   SELECT * FROM funcionarios
   ORDER BY Sobrenome DESC, Nome ASC;
   ```

6. **Como você consultaria os registros da tabela "clientes" ordenados em ordem alfabética crescente pelo nome, ignorando maiúsculas/minúsculas (ordem case-insensitive)?**

   ```sql
   SELECT * FROM clientes
   ORDER BY LOWER(Nome) ASC;
   ```

7. **Como você consultaria os registros da tabela "produtos" ordenados em ordem decrescente de preço, mas com os produtos de uma categoria específica agrupados e ordenados pelo preço dentro de cada categoria?**

   ```sql
   SELECT * FROM produtos
   WHERE Categoria = 'Eletrônicos'
   ORDER BY Categoria ASC, Preco DESC;
   ```



&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>