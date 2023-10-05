> **Função CEILING()**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você usaria a função CEILING() para arredondar o número decimal 56.372 para cima?

**Resposta 1:**
```sql
SELECT CEILING(56.372) AS 'Arredondado para cima';
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada "temperaturas" com uma coluna "temperatura_em_celsius" que armazena valores decimais. Como você usaria a função CEILING() para exibir todas as temperaturas arredondadas para cima?

**Resposta 2:**
```sql
SELECT temperatura_em_celsius, CEILING(temperatura_em_celsius) AS 'Arredondado para cima'
FROM temperaturas;
```

**Pergunta 3:** Qual é o resultado da função CEILING() quando aplicada ao número decimal 98.001?

**Resposta 3:**
```sql
SELECT CEILING(98.001) AS 'Arredondado para cima';
```

**Pergunta 4:** Se você tiver uma tabela chamada "alturas" com uma coluna "altura_em_metros" que armazena valores decimais, como você usaria a função CEILING() para exibir todas as alturas arredondadas para cima?

**Resposta 4:**
```sql
SELECT altura_em_metros, CEILING(altura_em_metros) AS 'Arredondado para cima'
FROM alturas;
```

**Pergunta 5:** Como você usaria a função CEILING() para arredondar o número decimal 123.456 para cima?

**Resposta 5:**
```sql
SELECT CEILING(123.456) AS 'Arredondado para cima';
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>