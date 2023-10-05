> **Criar e excluir índices**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria um índice único na coluna "CPF" da tabela "clientes"?

**Resposta 1:**
```sql
CREATE UNIQUE INDEX idx_cpf ON clientes (CPF);
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada "vendas" com um grande número de registros. Como você criaria um índice para a coluna "Data_Venda" para melhorar o desempenho das consultas que envolvem essa coluna?

**Resposta 2:**
```sql
CREATE INDEX idx_data_venda ON vendas (Data_Venda);
```

**Pergunta 3:** Você deseja criar um índice na tabela "produtos" para as colunas "Categoria" e "Nome". Como você faria isso em uma única instrução?

**Resposta 3:**
```sql
CREATE INDEX idx_categoria_nome ON produtos (Categoria, Nome);
```

**Pergunta 4:** Como você verificaria se a tabela "estoque" possui algum índice criado na coluna "ID_Produto"?

**Resposta 4:**
```sql
SHOW INDEX FROM estoque WHERE Column_name = 'ID_Produto';
```

**Pergunta 5:** Suponha que você tenha um índice chamado "idx_valor" na tabela "pedidos". Como você o excluiria?

**Resposta 5:**
```sql
DROP INDEX idx_valor ON pedidos;
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>