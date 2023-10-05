> **Gerenciar Contas de Usuários – Criar, Consultar, Renomear e Excluir**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você consultaria a tabela interna "User" no MySQL para listar todos os usuários existentes juntamente com seus respectivos hosts de conexão?

**Resposta 1:**
Você pode consultar a tabela interna "User" no MySQL para listar todos os usuários existentes juntamente com seus respectivos hosts de conexão usando a seguinte declaração SQL:

```sql
SELECT User, Host FROM mysql.user;
```

Isso retornará uma lista de usuários e os hosts a partir dos quais eles podem se conectar ao banco de dados.

**Pergunta 2:** Como você criaria um novo usuário chamado "joao" com senha "senhasegura" que pode se conectar apenas a partir do host local?

**Resposta 2:**
Você pode criar um novo usuário chamado "joao" com senha "senhasegura" que pode se conectar apenas a partir do host local da seguinte forma:

```sql
CREATE USER 'joao'@'localhost' IDENTIFIED BY 'senhasegura';
```

Isso cria o usuário "joao" com a senha especificada e restringe o acesso apenas ao host local.

**Pergunta 3:** Como você criaria um novo usuário chamado "ana" com senha "1234" que pode se conectar de qualquer host?

**Resposta 3:**
Você pode criar um novo usuário chamado "ana" com senha "1234" que pode se conectar de qualquer host da seguinte forma:

```sql
CREATE USER 'ana' IDENTIFIED BY '1234';
```

Isso permite que o usuário "ana" se conecte de qualquer lugar, pois não especificamos um host.

**Pergunta 4:** Como você alteraria a senha do usuário "marcos" para "novasenha" no MySQL?

**Resposta 4:**
Você pode alterar a senha do usuário "marcos" para "novasenha" no MySQL usando a seguinte declaração:

```sql
SET PASSWORD FOR 'marcos'@'localhost' = PASSWORD('novasenha');
```

Isso define a nova senha para o usuário "marcos" no host local.

**Pergunta 5:** Como você renomearia o usuário "carla" para "carolina" no MySQL?

**Resposta 5:**
Você pode renomear o usuário "carla" para "carolina" no MySQL usando a seguinte declaração:

```sql
RENAME USER 'carla' TO 'carolina';
```

Isso renomeia o usuário "carla" para "carolina" mantendo os privilégios configurados para o novo nome de usuário.

**Pergunta 6:** Como você excluiria o usuário "jose" do MySQL junto com todos os seus privilégios?

**Resposta 6:**
Você pode excluir o usuário "jose" do MySQL junto com todos os seus privilégios usando a seguinte declaração:

```sql
DROP USER 'jose';
```

Isso eliminará o usuário "jose" do sistema, juntamente com todos os privilégios associados a ele.

**Pergunta 7:** Como você criaria um novo usuário chamado "lucas" sem especificar uma senha no momento da criação?

**Resposta 7:**
Você pode criar um novo usuário chamado "lucas" sem especificar uma senha no momento da criação da seguinte forma:

```sql
CREATE USER 'lucas'@'localhost';
```

Isso cria o usuário "lucas" com acesso apenas a partir do host local (localhost) e sem senha definida. Você pode definir uma senha posteriormente, se desejar.

**Pergunta 8:** Como você criaria um novo usuário chamado "ana" com senha "12345" que pode se conectar a partir do host "exemplo.com"?

**Resposta 8:**
Você pode criar um novo usuário chamado "ana" com senha "12345" que pode se conectar a partir do host "exemplo.com" da seguinte forma:

```sql
CREATE USER 'ana'@'exemplo.com' IDENTIFIED BY '12345';
```

Isso permite que o usuário "ana" se conecte apenas a partir do host "exemplo.com".

**Pergunta 9:** Como você renomearia o usuário "roberto" para "robert" no MySQL?

**Resposta 9:**
Você pode renomear o usuário "roberto" para "robert" no MySQL usando a seguinte declaração:

```sql
RENAME USER 'roberto' TO 'robert';
```

Isso renomeia o usuário "roberto" para "robert" mantendo os privilégios configurados para o novo nome de usuário.

**Pergunta 10:** Como você excluiria o usuário "maria" do MySQL junto com todos os seus privilégios?

**Resposta 10:**
Você pode excluir o usuário "maria" do MySQL junto com todos os seus privilégios usando a seguinte declaração:



&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>