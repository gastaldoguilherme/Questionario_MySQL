> **Função TRUNCATE()**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você usaria a função TRUNCATE() para exibir o número 47.892 como 47?

**Resposta 1:**
```sql
SELECT TRUNCATE(47.892, 0) AS Truncado;
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada "precos_produtos" com uma coluna "preco" que armazena valores decimais. Como você usaria a função TRUNCATE() para exibir todos os preços com duas casas decimais?

**Resposta 2:**
```sql
SELECT TRUNCATE(preco, 2) AS PrecoTruncado
FROM precos_produtos;
```

**Pergunta 3:** Qual é a saída da função TRUNCATE() quando aplicada ao número 123.456 com 3 casas decimais?

**Resposta 3:**
```sql
SELECT TRUNCATE(123.456, 3) AS Truncado;
```

**Pergunta 4:** Se você tiver uma tabela chamada "pesos" com uma coluna "peso_em_quilos" que armazena valores decimais, como você usaria a função TRUNCATE() para exibir todos os pesos com zero casas decimais?

**Resposta 4:**
```sql
SELECT TRUNCATE(peso_em_quilos, 0) AS PesoInteiro
FROM pesos;
```

**Pergunta 5:** Como você usaria a função TRUNCATE() para exibir o valor monetário 789.1234 como 789.1?

**Resposta 5:**
```sql
SELECT TRUNCATE(789.1234, 1) AS ValorTruncado;
```

Essas perguntas e respostas demonstram o uso da função TRUNCATE() no MySQL para trazer valores truncados com um número específico de casas decimais.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>