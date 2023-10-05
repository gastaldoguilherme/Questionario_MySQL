> **CREATE DATABASE -  Criar banco de dados**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Criar um Novo Banco de Dados:**

1. **Como criar um novo banco de dados no MySQL usando SQL e qual é a sintaxe básica para isso?**

   **Resposta:** Para criar um novo banco de dados no MySQL, você pode usar o seguinte comando SQL:
   ```sql
   CREATE DATABASE IF NOT EXISTS nome_BD;
   ```
   Onde "nome_BD" é o nome que você deseja dar ao banco de dados. O elemento "IF NOT EXISTS" é opcional e evita o erro de tentar criar um banco de dados que já existe no servidor.

2. **Por que o uso do elemento "IF NOT EXISTS" é recomendado ao criar um banco de dados no MySQL?**

   **Resposta:** O uso de "IF NOT EXISTS" é recomendado ao criar um banco de dados para evitar erros caso o banco de dados com o mesmo nome já exista no servidor. Isso garante que não haja tentativas de criar bancos de dados duplicados.

**Verificar Bancos de Dados:**

3. **Como você pode verificar a lista de bancos de dados existentes no MySQL usando SQL?**

   **Resposta:** Você pode verificar os bancos de dados existentes no MySQL usando o seguinte comando SQL:
   ```sql
   SHOW DATABASES;
   ```

**Usar um Banco de Dados:**

4. **Qual é o propósito do comando SQL "USE" no MySQL e qual é a sintaxe básica para usá-lo?**

   **Resposta:** O comando "USE" instrui o Sistema de Gerenciamento de Banco de Dados Relacional (SGBDR) a utilizar o banco de dados especificado para executar os comandos. A sintaxe é a seguinte:
   ```sql
   USE nome_banco_de_dados;
   ```

5. **Como você pode verificar qual banco de dados está selecionado atualmente no MySQL?**

   **Resposta:** Para verificar o banco de dados selecionado no momento, você pode usar o seguinte comando SQL:
   ```sql
   SELECT DATABASE();
   ```

**Excluir Banco de Dados:**

6. **Como você pode excluir um banco de dados existente no MySQL usando SQL e qual é a sintaxe básica para isso?**

   **Resposta:** Para excluir um banco de dados existente, você pode usar o seguinte comando SQL:
   ```sql
   DROP DATABASE IF EXISTS nome_BD;
   ```
   O elemento "IF EXISTS" é opcional e evita erros caso o banco de dados não exista.

&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>