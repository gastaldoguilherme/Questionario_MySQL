> **DDL, DML, DCL, DQL, DTL - Grupos de Comandos SQL**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Grupos de Comandos SQL:**

1. **O que são comandos SQL e como eles são agrupados em categorias principais?**

   **Resposta:** Os comandos SQL são instruções utilizadas para interagir com bancos de dados. Eles são divididos em cinco grupos principais:
   - DDL (Data Definition Language): Usado para definir a estrutura do banco de dados, criar, alterar e excluir objetos como tabelas, views, triggers, procedimentos armazenados, etc.
   - DML (Data Manipulation Language): Utilizado para gerenciar os dados no banco, incluindo inserção, atualização e exclusão de registros.
   - DCL (Data Control Language): Responsável pelo controle de acesso aos dados por meio de permissões.
   - DQL (Data Query Language): Utilizado para realizar consultas e obter dados armazenados.
   - DTL (Data Transaction Language): Gerencia transações no banco de dados, permitindo commit, rollback e uso de savepoints.

**DDL – Data Definition Language:**

2. **Quais são alguns exemplos de comandos DDL e qual é a função de cada um deles?**

   **Resposta:** Alguns exemplos de comandos DDL incluem:
   - `CREATE`: Cria um novo banco de dados, tabela, visão, índice ou outro objeto no banco de dados.
   - `ALTER`: Modifica um objeto existente no banco de dados, como uma tabela.
   - `DROP`: Exclui uma tabela inteira, uma exibição de uma tabela ou outro objeto, incluindo o próprio banco de dados.

**DML – Data Manipulation Language:**

3. **O que é DML e quais são os comandos principais associados a ele?**

   **Resposta:** DML (Data Manipulation Language) é um grupo de comandos SQL usado para gerenciar os dados armazenados no banco de dados. Alguns comandos DML principais são:
   - `INSERT`: Cria um novo registro (linha) em uma tabela.
   - `UPDATE`: Modifica registros existentes em uma tabela.
   - `DELETE`: Exclui um ou mais registros de uma tabela.

**DCL – Data Control Language:**

4. **Qual é a finalidade dos comandos DCL em SQL e quais são alguns exemplos de comandos DCL?**

   **Resposta:** Comandos DCL (Data Control Language) são usados para controlar o acesso aos dados no banco de dados por meio de permissões. Alguns exemplos de comandos DCL incluem:
   - `GRANT`: Fornece privilégios de acesso a um usuário.
   - `REVOKE`: Retira os privilégios fornecidos a um usuário.
   - `ALTER USER`: Permite modificar contas de usuário, como alterar a senha de um usuário.

**DQL – Data Query Language:**

5. **O que é DQL e qual é o comando SQL principal associado a ele?**

   **Resposta:** DQL (Data Query Language) é um grupo de comandos SQL usado para realizar consultas em um banco de dados, obtendo dados armazenados. O comando SQL principal associado ao DQL é:
   - `SELECT`: Obtém registros especificados de uma ou mais tabelas, permitindo a realização de consultas em tabelas.

**DTL – Data Transaction Language:**

6. **Para que serve o grupo de comandos DTL em SQL e quais são alguns exemplos de comandos DTL?**

   **Resposta:** O grupo de comandos DTL (Data Transaction Language) é usado para gerenciar transações no banco de dados, controlando as alterações realizadas por comandos DML executados. Alguns exemplos de comandos DTL incluem:
   - `COMMIT`: Salva transações de forma permanente no banco de dados.
   - `ROLLBACK`: Restaura o banco ao último estado após um commit bem-sucedido.
   - `SAVEPOINT`: Salva temporariamente uma transação para possibilitar o rollback até aquele ponto, se necessário.

   
<div align="center">
   
[Retornar ao índice](/README.md)

</div>