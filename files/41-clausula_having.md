> **Cláusula HAVING**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


#**Pergunta 1:** Como você escreveria uma consulta que retorna o total de vendas das cidades com menos de 2500 produtos vendidos?

**Resposta 1:**
Você pode escrever uma consulta que retorna o total de vendas das cidades com menos de 2500 produtos vendidos da seguinte forma:

```sql
SELECT Cidade, SUM(Quantidade) As Total
FROM Vendas
GROUP BY Cidade
HAVING SUM(Quantidade) < 2500;
```

**Pergunta 2:** Como você modificaria a consulta para retornar o total de vendas do produto 'Teclado' nas cidades com menos de 1500 teclados vendidos?

**Resposta 2:**
Você pode modificar a consulta para retornar o total de vendas do produto 'Teclado' nas cidades com menos de 1500 teclados vendidos da seguinte forma:

```sql
SELECT Cidade, SUM(Quantidade) As TotalTeclados
FROM Vendas
WHERE Produto = 'Teclado'
GROUP BY Cidade
HAVING SUM(Quantidade) < 1500;
```
&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>