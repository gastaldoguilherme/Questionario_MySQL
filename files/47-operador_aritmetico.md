> **Funções Matemáticas e Operadores Aritméticos**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você calcularia o preço total de compra de 3 livros com preços diferentes da tabela `tbl_Livro`?

**Resposta 1:**
Você pode calcular o preço total de compra de 3 livros com preços diferentes da tabela `tbl_Livro` da seguinte forma:

```sql
SELECT SUM(Preco_Livro) AS 'Preço Total de Compra'
FROM tbl_Livro
LIMIT 3;
```

**Pergunta 2:** Como você calcularia o preço médio dos livros da tabela `tbl_Livro` após aplicar um desconto de 20% em cada preço?

**Resposta 2:**
Você pode calcular o preço médio dos livros da tabela `tbl_Livro` após aplicar um desconto de 20% em cada preço da seguinte forma:

```sql
SELECT AVG(Preco_Livro * 0.8) AS 'Preço Médio com Desconto'
FROM tbl_Livro;
```

**Pergunta 3:** Como você calcularia o valor do seno de 45 graus?

**Resposta 3:**
Você pode calcular o valor do seno de 45 graus da seguinte forma:

```sql
SELECT SIN(45 * PI() / 180) AS 'Seno de 45 graus';
```

**Pergunta 4:** Como você arredondaria para cima o valor da raiz quadrada de 20?

**Resposta 4:**
Você pode arredondar para cima o valor da raiz quadrada de 20 da seguinte forma:

```sql
SELECT CEILING(SQRT(20)) AS 'Raiz Quadrada de 20 Arredondada para Cima';
```

**Pergunta 5:** Como você calcularia o valor de 2 elevado à quarta potência?

**Resposta 5:**
Você pode calcular o valor de 2 elevado à quarta potência da seguinte forma:

```sql
SELECT POW(2, 4) AS '2 elevado à quarta potência';
```
&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>