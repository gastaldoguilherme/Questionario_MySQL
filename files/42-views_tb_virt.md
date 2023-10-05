> **VIEWS – Criando Tabelas Virtuais (Visões)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria uma view chamada `vw_Autores` que retorna os nomes dos autores da tabela `tbl_autores`?

**Resposta 1:**
Você pode criar uma view chamada `vw_Autores` que retorna os nomes dos autores da tabela `tbl_autores` com o seguinte comando:

```sql
CREATE VIEW vw_Autores
AS SELECT Nome_Autor
FROM tbl_autores;
```

**Pergunta 2:** Suponha que você deseje criar uma view chamada `vw_LivrosMaisCaros` que retorna os nomes e preços dos livros com preço superior a R$ 100. Como você faria isso?

**Resposta 2:**
Você pode criar uma view chamada `vw_LivrosMaisCaros` que retorna os nomes e preços dos livros com preço superior a R$ 100 da seguinte forma:

```sql
CREATE VIEW vw_LivrosMaisCaros
AS SELECT Nome_Livro AS Livro, Preco_Livro AS Preco
FROM tbl_Livro
WHERE Preco_Livro > 100.00;
```

**Pergunta 3:** Como você poderia listar todas as views existentes no banco de dados chamado `biblioteca`?

**Resposta 3:**
Você pode listar todas as views existentes no banco de dados `biblioteca` com o seguinte comando:

```sql
SHOW FULL TABLES IN biblioteca
WHERE TABLE_TYPE LIKE 'VIEW';
```

**Pergunta 4:** Como você excluiria a view `vw_Autores`?

**Resposta 4:**
Você pode excluir a view `vw_Autores` com o seguinte comando:

```sql
DROP VIEW vw_Autores;
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>