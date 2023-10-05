> **Concatenação de Strings: CONCAT, IFNULL e COALESCE**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você concatenaria os nomes dos autores da tabela `tbl_autores` com seus sobrenomes, incluindo um espaço entre eles, e renomearia a coluna resultante como 'Nome Completo'?

**Resposta 1:**
Você pode concatenar os nomes dos autores da tabela `tbl_autores` com seus sobrenomes e renomear a coluna resultante como 'Nome Completo' da seguinte forma:

```sql
SELECT CONCAT(Nome_autor, ' ', Sobrenome_autor) AS 'Nome Completo'
FROM tbl_autores;
```

**Pergunta 2:** Como você concatenaria a frase "Eu tenho 5 maçãs" usando a quantidade da tabela `teste_nulos` para o item 'Maçãs' e substituiria NULL por 0?

**Resposta 2:**
Você pode concatenar a frase "Eu tenho 5 maçãs" usando a quantidade da tabela `teste_nulos` para o item 'Maçãs' e substituir NULL por 0 da seguinte forma:

```sql
SELECT CONCAT('Eu tenho ', IFNULL(quantidade, 0), ' maçãs') AS frase_concatenada
FROM teste_nulos
WHERE item = 'Maçãs';
```

**Pergunta 3:** Como você concatenaria a frase "O preço é indefinido" usando o preço da tabela `teste_nulos` para o item 'Definido' e substituiria NULL por "indefinido"?

**Resposta 3:**
Você pode concatenar a frase "O preço é indefinido" usando o preço da tabela `teste_nulos` para o item 'Definido' e substituir NULL por "indefinido" da seguinte forma:

```sql
SELECT CONCAT('O preço é ', COALESCE(preco, 'indefinido')) AS frase_concatenada
FROM teste_nulos
WHERE item = 'Definido';
```
&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>