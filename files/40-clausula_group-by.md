> **Cláusula GROUP BY**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você obteria o total de vendas de Mouses (produto 'Mouse') sem usar a cláusula GROUP BY?

**Resposta 1:**
Você pode obter o total de vendas de Mouses sem usar a cláusula GROUP BY da seguinte forma:

```sql
SELECT SUM(Quantidade) As TotalMouses
FROM Vendas
WHERE Produto = 'Mouse';
```

**Pergunta 2:** Como você escreveria uma consulta que retorna o total de vendas para cada produto, agrupado por cidade?

**Resposta 2:**
Você pode escrever uma consulta que retorna o total de vendas para cada produto, agrupado por cidade, da seguinte forma:

```sql
SELECT Cidade, Produto, SUM(Quantidade) As Total
FROM Vendas
GROUP BY Cidade, Produto;
```

**Pergunta 3:** Como você obteria o número total de vendas (quantidade de registros) por cidade?

**Resposta 3:**
Você pode obter o número total de vendas (quantidade de registros) por cidade da seguinte forma:

```sql
SELECT Cidade, COUNT(*) As Total
FROM Vendas
GROUP BY Cidade;
```

**Pergunta 4:** Como você escreveria uma consulta que retorna o total de vendas realizadas por cada vendedor?

**Resposta 4:**
Você pode escrever uma consulta que retorna o total de vendas realizadas por cada vendedor da seguinte forma:

```sql
SELECT Nome_Vendedor, SUM(Quantidade) As TotalVendas
FROM Vendas
GROUP BY Nome_Vendedor;
```

**Pergunta 5:** Qual é a diferença entre usar a cláusula GROUP BY e a cláusula DISTINCT em uma consulta SELECT?

**Resposta 5:**
A cláusula GROUP BY é usada para agrupar registros com base em uma ou mais colunas e permite que você realize cálculos de agregação, como somas e contagens, nos grupos resultantes. Ela reduz o número de linhas retornadas na consulta, pois retorna um único registro para cada grupo.

A cláusula DISTINCT, por outro lado, é usada para retornar valores únicos em uma coluna específica, eliminando linhas duplicadas. Ela não realiza cálculos de agregação nos dados, apenas garante que os valores na coluna especificada sejam exclusivos.

Em resumo, o GROUP BY é usado para agrupar e agregar dados, enquanto o DISTINCT é usado para garantir a unicidade dos valores em uma coluna, sem agregação.


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>