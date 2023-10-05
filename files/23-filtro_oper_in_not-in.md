> **Operadores IN e NOT IN**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Escreva uma consulta SQL para retornar os nomes dos clientes que fizeram compras em janeiro ou fevereiro de 2023.

**Resposta 1:**
```sql
SELECT Nome_Cliente
FROM tbl_clientes
WHERE MONTH(Data_Compra) IN (1, 2) AND YEAR(Data_Compra) = 2023;
```

**Pergunta 2:** Crie uma consulta SQL para trazer os títulos dos filmes que têm uma classificação indicativa de 12 anos ou 14 anos.

**Resposta 2:**
```sql
SELECT Titulo_Filme
FROM tbl_filmes
WHERE Classificacao_Indicativa IN (12, 14);
```

**Pergunta 3:** Escreva uma consulta SQL para retornar os nomes dos produtos que estão em estoque (quantidade maior que zero) e cuja categoria seja "Eletrônicos" ou "Roupas".

**Resposta 3:**
```sql
SELECT Nome_Produto
FROM tbl_produtos
WHERE Quantidade_Estoque > 0
AND Categoria IN ('Eletrônicos', 'Roupas');
```

**Pergunta 4:** Crie uma consulta SQL que traga os nomes dos funcionários que têm o cargo de "Gerente" ou "Supervisor".

**Resposta 4:**
```sql
SELECT Nome_Funcionario
FROM tbl_funcionarios
WHERE Cargo IN ('Gerente', 'Supervisor');
```

**Pergunta 5:** Escreva uma consulta SQL para trazer os registros de vendas que foram realizadas no segundo trimestre do ano corrente (abril a junho).

**Resposta 5:**
```sql
SELECT *
FROM tbl_vendas
WHERE MONTH(Data_Venda) BETWEEN 4 AND 6 AND YEAR(Data_Venda) = YEAR(CURRENT_DATE());
```

Essas perguntas e respostas demonstram como utilizar os operadores IN e NOT IN para filtrar resultados de consultas SQL com base em listas de valores ou subconsultas.


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>