> **ALTER TABLE, DROP TABLE - Alterar Tabelas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



**1. Como você pode remover uma coluna de uma tabela no MySQL?**

   - Resposta: Você pode remover uma coluna de uma tabela no MySQL usando o comando `ALTER TABLE` da seguinte maneira:

   ```sql
   ALTER TABLE nome-tabela
   DROP COLUMN nome-coluna;
   ```

**2. Como você pode excluir uma chave primária de uma tabela no MySQL?**

   - Resposta: Você pode excluir uma chave primária de uma tabela no MySQL usando o comando `ALTER TABLE` da seguinte maneira:

   ```sql
   ALTER TABLE nome-tabela
   DROP PRIMARY KEY;
   ```

**3. Como você pode adicionar uma nova coluna a uma tabela no MySQL?**

   - Resposta: Você pode adicionar uma nova coluna a uma tabela no MySQL usando o comando `ALTER TABLE` da seguinte maneira:

   ```sql
   ALTER TABLE nome-tabela
   ADD nome-coluna tipo-de-dados constraints;
   ```

**4. Como você pode criar um relacionamento entre duas tabelas no MySQL usando o comando `ALTER TABLE`?**

   - Resposta: Você pode criar um relacionamento entre duas tabelas no MySQL usando o comando `ALTER TABLE` para adicionar uma restrição de chave estrangeira da seguinte maneira:

   ```sql
   ALTER TABLE tabela-de-origem
   ADD CONSTRAINT nome-constraint
   FOREIGN KEY (coluna-de-chave-estrangeira)
   REFERENCES tabela-de-destino (coluna-de-chave-primária)
   ON DELETE ação-referencial
   ON UPDATE ação-referencial;
   ```

**5. Como você pode modificar o tipo de dados de uma coluna existente no MySQL?**

   - Resposta: Você pode modificar o tipo de dados de uma coluna existente no MySQL usando o comando `ALTER TABLE` da seguinte maneira:

   ```sql
   ALTER TABLE nome-tabela
   MODIFY COLUMN nome-coluna novo-tipo-de-dados;
   ```

**6. Como você pode excluir completamente uma tabela no MySQL?**

   - Resposta: Você pode excluir completamente uma tabela no MySQL usando o comando `DROP TABLE` da seguinte maneira:

   ```sql
   DROP TABLE nome-tabela;
   ```

Lembre-se de ter cuidado ao executar comandos que excluem tabelas, pois isso apagará todos os dados na tabela permanentemente.


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>