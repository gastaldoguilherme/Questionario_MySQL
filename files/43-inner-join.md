> **INNER JOIN – Consultar dados em duas ou mais Tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você consultaria os nomes dos clientes e os produtos que eles compraram usando a cláusula INNER JOIN entre as tabelas `tbl_clientes` e `tbl_compras`?

**Resposta 1:**
Você pode consultar os nomes dos clientes e os produtos que eles compraram usando INNER JOIN da seguinte maneira:

```sql
SELECT C.Nome_Cliente, P.Nome_Produto
FROM tbl_clientes AS C
INNER JOIN tbl_compras AS Co
ON C.ID_Cliente = Co.ID_Cliente
INNER JOIN tbl_produtos AS P
ON Co.ID_Produto = P.ID_Produto;
```

**Pergunta 2:** Como você retornaria os nomes dos alunos e seus respectivos cursos, considerando as tabelas `tbl_alunos` e `tbl_cursos`?

**Resposta 2:**
Você pode retornar os nomes dos alunos e seus respectivos cursos usando INNER JOIN da seguinte maneira:

```sql
SELECT A.Nome_Aluno, C.Nome_Curso
FROM tbl_alunos AS A
INNER JOIN tbl_matriculas AS M
ON A.ID_Aluno = M.ID_Aluno
INNER JOIN tbl_cursos AS C
ON M.ID_Curso = C.ID_Curso;
```

**Pergunta 3:** Como você listaria os nomes dos funcionários e os nomes de seus gerentes com base nas tabelas `tbl_funcionarios` e `tbl_gestores`?

**Resposta 3:**
Você pode listar os nomes dos funcionários e os nomes de seus gerentes usando INNER JOIN da seguinte forma:

```sql
SELECT F.Nome_Funcionario, G.Nome_Gerente
FROM tbl_funcionarios AS F
INNER JOIN tbl_gestores AS G
ON F.ID_Gerente = G.ID_Gerente;
```

**Pergunta 4:** Suponha que você queira consultar os nomes dos produtos, suas categorias e os nomes dos fornecedores desses produtos. Como você faria isso usando INNER JOIN nas tabelas `tbl_produtos`, `tbl_categorias` e `tbl_fornecedores`?

**Resposta 4:**
Você pode consultar os nomes dos produtos, suas categorias e os nomes dos fornecedores usando INNER JOIN da seguinte maneira:

```sql
SELECT P.Nome_Produto, C.Nome_Categoria, F.Nome_Fornecedor
FROM tbl_produtos AS P
INNER JOIN tbl_categorias AS C
ON P.ID_Categoria = C.ID_Categoria
INNER JOIN tbl_fornecedores AS F
ON P.ID_Fornecedor = F.ID_Fornecedor;
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>