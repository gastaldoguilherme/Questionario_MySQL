> **Função FLOOR()**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você usaria a função FLOOR() para arredondar o número decimal 45.89 para baixo, mostrando apenas sua parte inteira?

**Resposta 1:**
```sql
SELECT FLOOR(45.89) AS Arredondado;
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada "vendas" com uma coluna "valor_total" que armazena valores decimais. Como você usaria a função FLOOR() para arredondar todos os valores na coluna "valor_total" para baixo, mostrando apenas a parte inteira?

**Resposta 2:**
```sql
SELECT FLOOR(valor_total) AS ValorInteiro
FROM vendas;
```

**Pergunta 3:** Qual é a quantidade total de produtos em estoque com preços menores ou iguais a 50.00 que você obteria usando a função FLOOR()?

**Resposta 3:**
```sql
SELECT COUNT(*) AS QuantidadeProdutos
FROM estoque
WHERE FLOOR(preco) <= 50.00;
```

**Pergunta 4:** Se você tiver uma tabela chamada "avaliacoes" com uma coluna "classificacao" que varia de 1 a 5, como você usaria a função FLOOR() para calcular a porcentagem de avaliações que são 4 ou 5?

**Resposta 4:**
```sql
SELECT (COUNT(*) / (SELECT COUNT(*) FROM avaliacoes)) * 100 AS 'Porcentagem de Avaliações 4 ou 5'
FROM avaliacoes
WHERE FLOOR(classificacao) >= 4;
```

**Pergunta 5:** Como você usaria a função FLOOR() para arredondar um valor monetário de 123.45 para baixo e mostrar apenas a parte inteira?

**Resposta 5:**
```sql
SELECT FLOOR(123.45) AS Arredondado;
```

Essas perguntas e respostas demonstram o uso da função FLOOR() no MySQL para arredondar valores para baixo e obter suas partes inteiras em várias situações.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>