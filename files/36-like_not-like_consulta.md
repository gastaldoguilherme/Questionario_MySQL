> **LIKE e NOT LIKE**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você selecionaria todos os registros da tabela `produtos` cujos nomes começam com a letra "A"?

**Resposta 1:**
```sql
SELECT *
FROM produtos
WHERE nome_produto LIKE 'A%';
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada `clientes` com coluna `nome_cliente`. Como você selecionaria todos os clientes cujos nomes terminam com a letra "o"?

**Resposta 2:**
```sql
SELECT *
FROM clientes
WHERE nome_cliente LIKE '%o';
```

**Pergunta 3:** Como você selecionaria todos os registros da tabela `estoque` onde o nome do produto contém a sequência "xyz" em qualquer posição da string?

**Resposta 3:**
```sql
SELECT *
FROM estoque
WHERE nome_produto LIKE '%xyz%';
```

**Pergunta 4:** Suponha que você tenha uma tabela chamada `funcionarios` com coluna `nome_funcionario`. Como você selecionaria todos os funcionários cujos nomes têm exatamente cinco caracteres?

**Resposta 4:**
```sql
SELECT *
FROM funcionarios
WHERE nome_funcionario LIKE '_____';
-- Cinco sublinhados representam qualquer nome com exatamente cinco caracteres.
```

**Pergunta 5:** Como você selecionaria todos os registros da tabela `vendas` onde o campo `descricao_produto` não contém a palavra "exemplo"?

**Resposta 5:**
```sql
SELECT *
FROM vendas
WHERE descricao_produto NOT LIKE '%exemplo%';
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>