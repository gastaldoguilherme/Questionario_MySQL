> **Tipo de Dados ENUM**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


1. **Como você cria uma coluna do tipo ENUM chamada "status_pedido" que pode armazenar os valores "pendente", "processando" e "entregue" em uma tabela chamada "pedidos"?**

   ```sql
   CREATE TABLE pedidos (
     id INT PRIMARY KEY AUTO_INCREMENT,
     status_pedido ENUM('pendente', 'processando', 'entregue')
   );
   ```

   Resposta:

   A coluna "status_pedido" agora pode armazenar um dos valores: "pendente", "processando" ou "entregue".

2. **Como você insere um novo pedido na tabela "pedidos" com o status "entregue"?**

   ```sql
   INSERT INTO pedidos (status_pedido)
   VALUES ('entregue');
   ```

   Resposta:

   Um novo pedido com o status "entregue" será inserido na tabela "pedidos".

3. **O que acontece se você tentar inserir um valor não permitido, como "cancelado", na coluna "status_pedido" da tabela "pedidos"?**

   Resposta:

   Ao tentar inserir um valor não permitido, como "cancelado", ocorrerá um erro e o registro não será inserido na tabela.

4. **Como você consulta os valores permitidos na coluna "status_pedido" da tabela "pedidos"?**

   ```sql
   SHOW COLUMNS
   FROM pedidos
   LIKE 'status_pedido';
   ```

   Resposta:

   Isso mostrará os valores permitidos na coluna "status_pedido" da tabela "pedidos".

5. **Como você ordena os registros na tabela "pedidos" pelo status de pedido em ordem alfabética crescente?**

   ```sql
   SELECT * FROM pedidos
   ORDER BY CAST(status_pedido AS CHAR);
   ```

   Resposta:

   Os registros na tabela "pedidos" serão ordenados pelo status de pedido em ordem alfabética crescente usando a função CAST.

6. **Quantos elementos podem ser atribuídos a uma coluna do tipo ENUM no MySQL?**

   Resposta:

   Uma coluna do tipo ENUM no MySQL pode ter no máximo 65.535 elementos atribuídos.

7. **Por que não é recomendado usar valores numéricos em uma coluna do tipo ENUM no MySQL?**

   Resposta:

   Não é recomendado usar valores numéricos em uma coluna do tipo ENUM no MySQL porque não há economia de espaço de armazenamento em comparação com valores SMALLINT ou TINYINT, e isso pode causar confusão entre o valor armazenado e o número interno usado para representá-lo.



&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>