> **Funções de Agregação (MAX, MIN, AVG, COUNT, SUM) **     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você contaria o número total de produtos na tabela "produtos"?

**Resposta 1:**
```sql
SELECT COUNT(*) FROM produtos;
```

**Pergunta 2:** Qual é o preço médio dos produtos na categoria "Eletrônicos"?

**Resposta 2:**
```sql
SELECT AVG(Preco) FROM produtos WHERE Categoria = 'Eletrônicos';
```

**Pergunta 3:** Qual é o produto mais caro na tabela "produtos"?

**Resposta 3:**
```sql
SELECT MAX(Preco) FROM produtos;
```

**Pergunta 4:** Quantos pedidos foram feitos pelo cliente com ID igual a 5?

**Resposta 4:**
```sql
SELECT COUNT(*) FROM pedidos WHERE ID_Cliente = 5;
```

**Pergunta 5:** Qual é o valor total de vendas para cada mês do ano de 2023?

**Resposta 5:**
```sql
SELECT MONTH(Data_Venda) AS Mes, SUM(Valor_Venda) AS Total
FROM vendas
WHERE YEAR(Data_Venda) = 2023
GROUP BY Mes;
```

Essas perguntas e respostas demonstram como usar funções de agregação comuns como COUNT, AVG, MAX, SUM e MIN para obter informações úteis de um banco de dados MySQL. As consultas podem ser adaptadas para atender às necessidades específicas de análise de dados.


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>