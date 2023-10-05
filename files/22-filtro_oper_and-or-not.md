> **Operadores AND, OR e NOT**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Escreva uma consulta SQL para retornar os nomes dos clientes que fizeram compras nos últimos 30 dias e cujo valor total gasto seja superior a 500 dólares.

**Resposta 1:**
```sql
SELECT Nome_Cliente
FROM tbl_clientes
WHERE Data_Ultima_Compra >= DATE_SUB(NOW(), INTERVAL 30 DAY)
AND Valor_Total_Gasto > 500;
```

**Pergunta 2:** Crie uma consulta SQL para trazer os títulos dos filmes que têm uma classificação indicativa menor que 14 anos e que foram lançados após 2010.

**Resposta 2:**
```sql
SELECT Titulo_Filme
FROM tbl_filmes
WHERE Classificacao_Indicativa < 14
AND YEAR(Data_Lancamento) > 2010;
```

**Pergunta 3:** Escreva uma consulta SQL para retornar os nomes dos produtos que estão em estoque (quantidade maior que zero) e cujo preço de venda não é superior a 50 dólares.

**Resposta 3:**
```sql
SELECT Nome_Produto
FROM tbl_produtos
WHERE Quantidade_Estoque > 0
AND Preco_Venda <= 50;
```

**Pergunta 4:** Crie uma consulta SQL que traga os nomes dos funcionários que não são gerentes e que têm menos de 5 anos de experiência.

**Resposta 4:**
```sql
SELECT Nome_Funcionario
FROM tbl_funcionarios
WHERE Nivel_Cargo != 'Gerente'
AND Anos_Experiencia < 5;
```

**Pergunta 5:** Escreva uma consulta SQL para trazer os registros de vendas que foram realizadas no primeiro trimestre do ano corrente (janeiro a março).

**Resposta 5:**
```sql
SELECT *
FROM tbl_vendas
WHERE Data_Venda >= '2023-01-01' AND Data_Venda <= '2023-03-31';
```

Essas perguntas e respostas demonstram como utilizar os operadores AND, OR e NOT para filtrar resultados de consultas SQL com base em múltiplas condições.


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>