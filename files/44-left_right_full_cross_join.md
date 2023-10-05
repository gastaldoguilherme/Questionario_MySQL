> **LEFT e RIGHT JOIN – Consultar dados em duas ou mais tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você consultaria todos os autores, mesmo aqueles que não têm livros publicados, usando LEFT JOIN entre as tabelas `tbl_autores` e `tbl_Livro`?

**Resposta 1:**
Você pode consultar todos os autores, mesmo aqueles que não têm livros publicados, usando LEFT JOIN da seguinte maneira:

```sql
SELECT * FROM tbl_autores
LEFT JOIN tbl_Livro
ON tbl_autores.ID_Autor = tbl_Livro.ID_Autor;
```

**Pergunta 2:** Como você retornaria todas as editoras, incluindo aquelas que não possuem livros publicados, usando RIGHT JOIN entre as tabelas `tbl_Livro` e `tbl_editoras`?

**Resposta 2:**
Você pode retornar todas as editoras, incluindo aquelas que não possuem livros publicados, usando RIGHT JOIN da seguinte forma:

```sql
SELECT * FROM tbl_Livro AS Li
RIGHT JOIN tbl_editoras AS Ed
ON Li.ID_editora = Ed.ID_editora;
```

**Pergunta 3:** Como você encontraria todas as combinações possíveis entre os nomes de produtos e os nomes de autores usando CROSS JOIN entre as tabelas `tbl_livro` e `tbl_autores`?

**Resposta 3:**
Você pode encontrar todas as combinações possíveis entre os nomes de produtos e os nomes de autores usando CROSS JOIN da seguinte forma:

```sql
SELECT Nome_Livro, Nome_Autor
FROM tbl_livro
CROSS JOIN tbl_autores;
```

**Pergunta 4:** Como você retornaria todas as editoras que não têm livros publicados, usando RIGHT JOIN e excluindo as correspondências, entre as tabelas `tbl_Livro` e `tbl_editoras`?

**Resposta 4:**
Para retornar todas as editoras que não têm livros publicados usando RIGHT JOIN e excluindo as correspondências, você pode fazer o seguinte:

```sql
SELECT * FROM tbl_Livro
RIGHT JOIN tbl_editoras
ON tbl_Livro.ID_editora = tbl_editoras.ID_editora
WHERE tbl_Livro.ID_editora IS NULL;
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>