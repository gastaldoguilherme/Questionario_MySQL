> **Tipo de Dados SET**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



1. **Como você cria uma tabela chamada "pedidos" com uma coluna "tempero" do tipo SET que pode armazenar os valores "Azeite", "Vinagre", "Sal", "Orégano" e "Pimenta"?**

   ```sql
   CREATE TABLE pedidos (
     idPedido SMALLINT PRIMARY KEY AUTO_INCREMENT,
     tempero SET ('Azeite','Vinagre','Sal','Orégano','Pimenta')
   );
   ```

   Resposta:

   A tabela "pedidos" com a coluna "tempero" do tipo SET é criada e pode armazenar os valores mencionados.

2. **Como você insere um novo pedido na tabela "pedidos" com o lanche "Frango" e os temperos "Sal" e "Orégano"?**

   ```sql
   INSERT INTO pedidos (lanche, tempero)
   VALUES ('Frango', 'Sal,Orégano');
   ```

   Resposta:

   Um novo pedido com o lanche "Frango" e os temperos "Sal" e "Orégano" será inserido na tabela "pedidos".

3. **O que acontece se você tentar inserir um valor não permitido, como "Mostarda", na coluna "tempero" da tabela "pedidos"?**

   Resposta:

   Ao tentar inserir um valor não permitido, como "Mostarda", ocorrerá um erro e o registro não será inserido na tabela.

4. **Como você consulta os pedidos que devem levar o tempero "Azeite"?**

   Usando operador LIKE:

   ```sql
   SELECT * FROM pedidos
   WHERE tempero LIKE '%Azeite%';
   ```

   Usando a função FIND_IN_SET():

   ```sql
   SELECT * FROM pedidos
   WHERE FIND_IN_SET('Azeite', tempero) > 0;
   ```

   Resposta:

   Isso retornará os pedidos que incluem o tempero "Azeite".

5. **Como você consulta os pedidos que possuem mais de um tempero, como por exemplo, lanches que levam "Pimenta" e "Azeite"?**

   ```sql
   SELECT * FROM pedidos
   WHERE tempero LIKE '%Pimenta%' AND tempero LIKE '%Azeite%';
   ```

   Resposta:

   Isso retornará os pedidos que incluem tanto "Pimenta" quanto "Azeite" como temperos.





&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>