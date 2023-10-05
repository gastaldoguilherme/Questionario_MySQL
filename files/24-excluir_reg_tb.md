> **DELETE e TRUNCATE TABLE - Excluir Registros de uma Tabela**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Escreva uma consulta SQL para excluir todos os registros da tabela "pedidos" onde o status do pedido seja "Cancelado".

**Resposta 1:**
```sql
DELETE FROM pedidos
WHERE status_pedido = 'Cancelado';
```

**Pergunta 2:** Crie uma consulta SQL para excluir todos os registros da tabela "itens_venda" onde a quantidade de itens vendidos seja igual a zero.

**Resposta 2:**
```sql
DELETE FROM itens_venda
WHERE quantidade_vendida = 0;
```

**Pergunta 3:** Escreva uma consulta SQL para excluir todos os registros da tabela "logs_acesso" que tenham mais de um ano de idade (ou seja, com data anterior a um ano atrás).

**Resposta 3:**
```sql
DELETE FROM logs_acesso
WHERE data_acesso < DATE_SUB(NOW(), INTERVAL 1 YEAR);
```

**Pergunta 4:** Crie uma consulta SQL para excluir um único registro da tabela "clientes" onde o ID do cliente seja 5.

**Resposta 4:**
```sql
DELETE FROM clientes
WHERE id_cliente = 5;
```

**Pergunta 5:** Escreva uma consulta SQL para excluir todos os registros da tabela "produtos" usando o comando TRUNCATE TABLE.

**Resposta 5:**
```sql
TRUNCATE TABLE produtos;
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>