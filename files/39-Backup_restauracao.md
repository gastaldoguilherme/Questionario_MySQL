> **Backup e restauração de bancos de dados**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você faria um backup de um banco de dados chamado `meubanco` usando o MySQL Workbench?

**Resposta 1:**
No MySQL Workbench, você pode fazer um backup de um banco de dados seguindo os passos abaixo:

1. Abra o MySQL Workbench e conecte-se ao servidor MySQL.
2. No painel do lado esquerdo, clique com o botão direito do mouse sobre o banco de dados `meubanco`.
3. Selecione a opção "Backup".
4. Escolha o local onde deseja salvar o arquivo de backup e defina um nome para o arquivo, por exemplo, `backup_meubanco.sql`.
5. Clique em "Iniciar Backup" para iniciar o processo de backup.

**Pergunta 2:** Como você faria a restauração de um banco de dados a partir de um arquivo de backup chamado `backup_meubanco.sql` usando o MySQL Workbench?

**Resposta 2:**
No MySQL Workbench, você pode restaurar um banco de dados a partir de um arquivo de backup seguindo os passos abaixo:

1. Abra o MySQL Workbench e conecte-se ao servidor MySQL.
2. No painel do lado esquerdo, clique com o botão direito do mouse sobre o banco de dados para o qual deseja restaurar os dados.
3. Selecione a opção "Restore".
4. Na janela de restauração, escolha a opção "Import from Self-Contained File".
5. Clique em "... (três pontos)" para selecionar o arquivo de backup, no caso, `backup_meubanco.sql`.
6. Clique em "Start Restore" para iniciar o processo de restauração.

**Pergunta 3:** Como você faria um backup de um banco de dados chamado `meubanco` usando o terminal (linha de comando) no MySQL?

**Resposta 3:**
Para fazer um backup de um banco de dados chamado `meubanco` usando o terminal (linha de comando) no MySQL, você pode usar o comando `mysqldump` da seguinte forma:

```bash
mysqldump -u root -p meubanco > backup_meubanco.sql
```

Isso irá criar um arquivo de backup chamado `backup_meubanco.sql` que contém os dados do banco de dados `meubanco`.

**Pergunta 4:** Como você faria a restauração de um banco de dados a partir de um arquivo de backup chamado `backup_meubanco.sql` usando o terminal (linha de comando) no MySQL?

**Resposta 4:**
Para restaurar um banco de dados a partir de um arquivo de backup chamado `backup_meubanco.sql` usando o terminal (linha de comando) no MySQL, você pode usar o seguinte comando:

```bash
mysql -u root -p meubanco < backup_meubanco.sql
```

Isso irá restaurar os dados do arquivo de backup para o banco de dados `meubanco`. Certifique-se de que o banco de dados `meubanco` já esteja criado antes de executar este comando.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>