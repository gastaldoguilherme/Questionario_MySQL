> **UPDATE – Modificar Registros em Tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você usaria o comando `UPDATE` para alterar o nome de um livro na tabela `tbl_Livros` com um `ID_LIVRO` igual a 5 para "Aventuras Incríveis"?

**Resposta 1:**
```sql
UPDATE tbl_Livros
SET Nome_Livro = 'Aventuras Incríveis'
WHERE ID_LIVRO = 5;
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada `tbl_Clientes` e deseja atualizar o número de telefone do cliente com um `ID_Cliente` igual a 101 para "(123) 456-7890". Como você faria isso usando o comando `UPDATE`?

**Resposta 2:**
```sql
UPDATE tbl_Clientes
SET Numero_Telefone = '(123) 456-7890'
WHERE ID_Cliente = 101;
```

**Pergunta 3:** Qual é a sintaxe correta para aumentar o preço de um livro com um ISBN13 de "9780735640610" para R$ 49,99 na tabela `tbl_Livros`?

**Resposta 3:**
```sql
UPDATE tbl_Livros
SET Preco_Livro = 49.99
WHERE ISBN13 = '9780735640610';
```

**Pergunta 4:** Se você tiver uma tabela chamada `tbl_Produtos` e quiser atualizar a descrição do produto com um `ID_Produto` igual a 7 para "Produto de Alta Qualidade", como você usaria o comando `UPDATE`?

**Resposta 4:**
```sql
UPDATE tbl_Produtos
SET Descricao = 'Produto de Alta Qualidade'
WHERE ID_Produto = 7;
```

**Pergunta 5:** Como você usaria o comando `UPDATE` para alterar o endereço de um cliente na tabela `tbl_Clientes` com `ID_Cliente` igual a 202 para "123 Main Street, Apt 4B"?

**Resposta 5:**
```sql
UPDATE tbl_Clientes
SET Endereco = '123 Main Street, Apt 4B'
WHERE ID_Cliente = 202;
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>