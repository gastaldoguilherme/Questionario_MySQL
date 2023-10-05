> **SELECT + RAND() - Retornar Linhas Aleatórias**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

1. **Como você retornaria um número inteiro aleatório entre 1 e 100 em uma consulta SQL no MySQL?**

   ```sql
   SELECT FLOOR(1 + RAND() * 100) AS Numero_Aleatorio;
   ```

   Resposta:

   A consulta retornará um número inteiro aleatório entre 1 e 100.

2. **Como você retornaria três registros aleatórios da tabela "produtos" em uma consulta SQL no MySQL?**

   ```sql
   SELECT * FROM produtos
   ORDER BY RAND()
   LIMIT 3;
   ```

   Resposta:

   A consulta retornará três registros aleatórios da tabela "produtos" toda vez que for executada.

3. **Como você retornaria uma amostra aleatória de 5% dos registros de uma grande tabela chamada "grandes_dados" em uma consulta SQL no MySQL?**

   ```sql
   SELECT * FROM grandes_dados
   WHERE RAND() <= 0.05;
   ```

   Resposta:

   A consulta retornará uma amostra aleatória de aproximadamente 5% dos registros da tabela "grandes_dados".

4. **Como você retornaria registros aleatórios da tabela "clientes" ordenados por seus IDs de cliente em ordem crescente?**

   ```sql
   SELECT * FROM clientes
   ORDER BY RAND() ASC;
   ```

   Resposta:

   A consulta retornará registros aleatórios da tabela "clientes" ordenados por seus IDs de cliente em ordem crescente.

5. **Como você retornaria registros aleatórios da tabela "pedidos" ordenados primeiro pelo nome do produto em ordem alfabética crescente e, em seguida, por uma classificação aleatória?**

   ```sql
   SELECT * FROM pedidos
   ORDER BY Nome_Produto ASC, RAND();
   ```

   Resposta:

   A consulta retornará registros da tabela "pedidos" ordenados pelo nome do produto em ordem alfabética crescente e, em seguida, aleatoriamente dentro de cada grupo de produtos com o mesmo nome.

Lembre-se de que, ao usar a função RAND() combinada com a cláusula ORDER BY em consultas em tabelas grandes, pode haver um impacto na performance do banco de dados, conforme mencionado no texto. Portanto, é importante considerar esse impacto ao aplicar essa técnica.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>