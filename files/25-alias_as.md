> **ALIAS - AS (Apelido)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria um alias para a coluna "Data_Publicacao" na tabela "livros" com o nome de "Data de Publicação"?

**Resposta 1:**
```sql
SELECT Data_Publicacao AS 'Data de Publicação'
FROM livros;
```

**Pergunta 2:** Crie uma consulta SQL que retorne o nome e o sobrenome do autor da tabela "autores" como um único alias chamado "Nome Completo".

**Resposta 2:**
```sql
SELECT CONCAT(Nome, ' ', Sobrenome) AS 'Nome Completo'
FROM autores;
```

**Pergunta 3:** Como você aplicaria um alias à tabela "pedidos" para chamá-la de "ordens" em uma consulta SQL?

**Resposta 3:**
```sql
SELECT *
FROM pedidos AS ordens;
```

**Pergunta 4:** Crie uma consulta SQL que retorne o nome do cliente e o valor total da compra (preço multiplicado pela quantidade) com os aliases "Cliente" e "Valor Total" a partir das tabelas "clientes" e "itens_compra". Certifique-se de unir essas tabelas apropriadamente.

**Resposta 4:**
```sql
SELECT c.Nome AS 'Cliente', SUM(ic.Preco * ic.Quantidade) AS 'Valor Total'
FROM clientes c
JOIN itens_compra ic ON c.id = ic.id_cliente
GROUP BY c.Nome;
```

**Pergunta 5:** Escreva uma consulta SQL que retorne o nome do produto da tabela "produtos" com o alias "Item" e sua quantidade total vendida na tabela "vendas" com o alias "Quantidade Vendida".

**Resposta 5:**
```sql
SELECT p.Nome AS 'Item', SUM(v.Quantidade) AS 'Quantidade Vendida'
FROM produtos p
JOIN vendas v ON p.id = v.id_produto
GROUP BY p.Nome;
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>