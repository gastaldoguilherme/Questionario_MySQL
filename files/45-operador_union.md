> **Operador UNION**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você consultaria nomes e categorias de produtos da tabela `tbl_produtos` e nomes e preços de produtos da tabela `tbl_preco_produtos`, combinando os resultados usando UNION?

**Resposta 1:**
Você pode consultar nomes e categorias de produtos da tabela `tbl_produtos` e nomes e preços de produtos da tabela `tbl_preco_produtos` combinando os resultados usando UNION da seguinte maneira:

```sql
SELECT Nome, Categoria
FROM tbl_produtos
UNION
SELECT Nome, Preco
FROM tbl_preco_produtos;
```

**Pergunta 2:** Como você retornaria nomes de funcionários da tabela `tbl_funcionarios` e nomes de clientes da tabela `tbl_clientes`, incluindo uma coluna adicional para identificar se são funcionários ou clientes, combinando os resultados usando UNION?

**Resposta 2:**
Você pode retornar nomes de funcionários da tabela `tbl_funcionarios` e nomes de clientes da tabela `tbl_clientes`, incluindo uma coluna adicional para identificar se são funcionários ou clientes, combinando os resultados usando UNION da seguinte forma:

```sql
SELECT Nome, 'Funcionário' AS Tipo
FROM tbl_funcionarios
UNION
SELECT Nome, 'Cliente' AS Tipo
FROM tbl_clientes;
```

**Pergunta 3:** Como você consultaria nomes de alunos da tabela `tbl_alunos` e nomes de professores da tabela `tbl_professores`, combinando os resultados usando UNION e garantindo que os resultados não contenham duplicatas?

**Resposta 3:**
Você pode consultar nomes de alunos da tabela `tbl_alunos` e nomes de professores da tabela `tbl_professores`, combinando os resultados usando UNION DISTINCT da seguinte forma:

```sql
SELECT Nome
FROM tbl_alunos
UNION DISTINCT
SELECT Nome
FROM tbl_professores;
```

**Pergunta 4:** Como você retornaria nomes e datas de nascimento de pessoas da tabela `tbl_pessoas` e nomes e endereços de empresas da tabela `tbl_empresas`, incluindo uma coluna adicional para identificar se são pessoas ou empresas, combinando os resultados usando UNION?

**Resposta 4:**
Você pode retornar nomes e datas de nascimento de pessoas da tabela `tbl_pessoas` e nomes e endereços de empresas da tabela `tbl_empresas`, incluindo uma coluna adicional para identificar se são pessoas ou empresas, combinando os resultados usando UNION da seguinte forma:

```sql
SELECT Nome, Data_Nascimento, 'Pessoa' AS Tipo
FROM tbl_pessoas
UNION
SELECT Nome, Endereco, 'Empresa' AS Tipo
FROM tbl_empresas;
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>