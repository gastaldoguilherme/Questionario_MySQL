> **BETWEEN – Seleção de intervalos em consultas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você usaria a cláusula `BETWEEN` para selecionar todos os registros da tabela `produtos` cujos preços estejam entre R$ 10,00 e R$ 20,00?

**Resposta 1:**
```sql
SELECT *
FROM produtos
WHERE preco BETWEEN 10.00 AND 20.00;
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada `pedidos` com colunas `ID_Pedido`, `Data_Pedido` e `Valor_Total`. Como você usaria a cláusula `BETWEEN` para selecionar todos os pedidos feitos entre 01/01/2022 e 31/12/2022?

**Resposta 2:**
```sql
SELECT *
FROM pedidos
WHERE Data_Pedido BETWEEN '2022-01-01' AND '2022-12-31';
```

**Pergunta 3:** Como você selecionaria todos os registros da tabela `estoque` onde a quantidade de produtos esteja entre 50 e 100 unidades?

**Resposta 3:**
```sql
SELECT *
FROM estoque
WHERE quantidade BETWEEN 50 AND 100;
```

**Pergunta 4:** Suponha que você tenha uma tabela chamada `funcionarios` com colunas `ID_Funcionario`, `Nome` e `Salario`. Como você usaria a cláusula `BETWEEN` para selecionar todos os funcionários com salários entre R$ 3000,00 e R$ 5000,00?

**Resposta 4:**
```sql
SELECT *
FROM funcionarios
WHERE Salario BETWEEN 3000.00 AND 5000.00;
```

**Pergunta 5:** Como você selecionaria todos os registros da tabela `vendas` onde o valor da venda está entre $1000 e $2000?

**Resposta 5:**
```sql
SELECT *
FROM vendas
WHERE valor_venda BETWEEN 1000 AND 2000;
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>