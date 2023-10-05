> **Função ROUND()**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você arredondaria o valor 123.45678 para três casas decimais?

**Resposta 1:**
```sql
SELECT ROUND(123.45678, 3) AS Arredondado;
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada "estoque" com uma coluna "quantidade" que armazena números decimais. Como você arredondaria todos os valores dessa coluna para a parte inteira?

**Resposta 2:**
```sql
SELECT ROUND(quantidade) AS QuantidadeArredondada
FROM estoque;
```

**Pergunta 3:** Qual é o preço médio arredondado para duas casas decimais dos produtos na categoria "Eletrônicos"?

**Resposta 3:**
```sql
SELECT ROUND(AVG(Preco), 2) AS 'Preço Médio Eletrônicos'
FROM produtos
WHERE Categoria = 'Eletrônicos';
```

**Pergunta 4:** Como você arredondaria todos os valores na coluna "valor" de uma tabela chamada "transacoes" para zero casas decimais?

**Resposta 4:**
```sql
SELECT ROUND(valor, 0) AS ValorArredondado
FROM transacoes;
```

**Pergunta 5:** Se você tiver uma tabela chamada "avaliacoes" com uma coluna "classificacao" que varia de 1 a 5, como você arredondaria a média das classificações para a parte inteira?

**Resposta 5:**
```sql
SELECT ROUND(AVG(classificacao)) AS 'Classificação Média'
FROM avaliacoes;
```

Essas perguntas e respostas ilustram como usar a função ROUND() em consultas SQL no MySQL para arredondar valores conforme suas necessidades, seja para um número específico de casas decimais ou para a parte inteira.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>