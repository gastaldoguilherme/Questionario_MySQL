> **GRANT e REVOKE – Definindo privilégios de acesso aos bancos de dados no MySQL**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



**Pergunta 1:** Como você atribuiria o privilégio "INSERT" na tabela "produtos" do banco de dados "ecommerce" ao usuário "vendedor" com senha "senha123"?

**Resposta 1:**
```sql
GRANT INSERT
ON ecommerce.produtos
TO 'vendedor'@'localhost' IDENTIFIED BY 'senha123';
```

**Pergunta 2:** Como você revogaria o privilégio "UPDATE" na tabela "pedidos" do banco de dados "ecommerce" do usuário "cliente"?

**Resposta 2:**
```sql
REVOKE UPDATE
ON ecommerce.pedidos
FROM 'cliente'@'localhost';
```

**Pergunta 3:** Como você atribuiria todos os privilégios disponíveis no nível global ao usuário "admin" com senha "admin123"?

**Resposta 3:**
```sql
GRANT ALL PRIVILEGES
ON *.*
TO 'admin'@'localhost' IDENTIFIED BY 'admin123' WITH GRANT OPTION;
```

**Pergunta 4:** Como você revogaria todos os privilégios do usuário "analista" em todas as tabelas e bancos de dados?

**Resposta 4:**
```sql
REVOKE ALL PRIVILEGES
ON *.*
FROM 'analista'@'localhost';
```

**Pergunta 5:** Como você atribuiria os privilégios "CREATE" e "DROP" no banco de dados "rhdb" ao usuário "dba"?

**Resposta 5:**
```sql
GRANT CREATE, DROP
ON rhdb.*
TO 'dba'@'localhost';
```

**Pergunta 6:** Como você revogaria o privilégio "SHOW DATABASES" do usuário "visitante"?

**Resposta 6:**
```sql
REVOKE SHOW DATABASES
ON *.*
FROM 'visitante'@'localhost';
```

**Pergunta 7:** Como você atribuiria o privilégio "SELECT" nas colunas "nome" e "email" da tabela "clientes" no banco de dados "crm" ao usuário "suporte"?

**Resposta 7:**
```sql
GRANT SELECT (nome, email)
ON crm.clientes
TO 'suporte'@'localhost';
```

**Pergunta 8:** Como você revogaria o privilégio "DELETE" da tabela "registros" no banco de dados "arquivos" do usuário "editor"?

**Resposta 8:**
```sql
REVOKE DELETE
ON arquivos.registros
FROM 'editor'@'localhost';
```

**Pergunta 9:** Como você atribuiria o privilégio "CREATE ROUTINE" ao usuário "desenvolvedor" no MySQL?

**Resposta 9:**
```sql
GRANT CREATE ROUTINE
ON *.*
TO 'desenvolvedor'@'localhost';
```

**Pergunta 10:** Como você revogaria o privilégio "ALTER" na tabela "funcionarios" do banco de dados "rhdb" do usuário "gestor"?

**Resposta 10:**
```sql
REVOKE ALTER
ON rhdb.funcionarios
FROM 'gestor'@'localhost';
```

**Pergunta 11:** Como você atribuiria o privilégio "INDEX" na tabela "produtos" do banco de dados "ecommerce" ao usuário "desenvolvedor"?

**Resposta 11:**
```sql
GRANT INDEX
ON ecommerce.produtos
TO 'desenvolvedor'@'localhost';
```

**Pergunta 12:** Como você revogaria todos os privilégios do usuário "usuario1" no banco de dados "db1" do MySQL?

**Resposta 12:**
```sql
REVOKE ALL PRIVILEGES
ON db1.*
FROM 'usuario1'@'localhost';
```

**Pergunta 13:** Como você atribuiria o privilégio "TRIGGER" na tabela "logs" do banco de dados "appdb" ao usuário "auditor"?

**Resposta 13:**
```sql
GRANT TRIGGER
ON appdb.logs
TO 'auditor'@'localhost';
```

**Pergunta 14:** Como você revogaria todos os privilégios de todas as tabelas e bancos de dados do usuário "teste"?

**Resposta 14:**
```sql
REVOKE ALL PRIVILEGES
ON *.*
FROM 'teste'@'localhost';
```

**Pergunta 15:** Como você atribuiria o privilégio "USAGE" ao usuário "convidado" no MySQL?

**Resposta 15:**
```sql
GRANT USAGE
ON *.*
TO 'convidado'@'localhost';
```

**Pergunta 16:** Como você revogaria o privilégio "CREATE USER" do usuário "admin" no MySQL?

**Resposta 16:**
```sql
REVOKE CREATE USER
ON *.*
FROM 'admin'@'localhost';
```

**Pergunta 17:** Como você atribuiria o privilégio "RELOAD" ao usuário "backup" no MySQL?

**Resposta 17:**
```sql
GRANT RELOAD
ON *.*
TO 'backup'@'localhost';
```

**Pergunta 18:** Como você revogaria o privilégio "ALTER ROUTINE" do usuário "desenvolvedor" no MySQL?

**Resposta 18:**
```sql
REVOKE ALTER ROUTINE
ON *.*
FROM 'desenvolvedor'@'localhost';
```

**Pergunta 19:** Como você atribuiria o privilégio "SHOW DATABASES" ao usuário "analista" no MySQL?

**Resposta 19:**
```sql
GRANT SHOW DATABASES
ON *.*
TO 'analista'@'localhost';
```

**Pergunta 20:** Como você revogaria todos os privilégios administrativos do usuário "admin" no MySQL?

**Resposta 20:**
```sql
REVOKE CREATE USER, SHOW DATABASES, SHUTDOWN, RELOAD
ON *.*
FROM 'admin'@'localhost';
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>