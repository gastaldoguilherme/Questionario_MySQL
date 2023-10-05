> **FOREIGN KEY (Chave Estrangeira)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**1. Como criar uma tabela "Pai" e uma tabela "Filho" com uma chave estrangeira "filho" que utiliza a opção ON DELETE CASCADE?**

```sql
-- Criação do Banco de Dados "testes"
CREATE DATABASE testes;
USE testes;

-- Criação da tabela "Pai" com chave primária ID_Pai
CREATE TABLE Pai (
 ID_Pai SMALLINT PRIMARY KEY,
 Nome_Pai VARCHAR(50)
);

-- Criação da tabela "Filho" com chave estrangeira "filho" que utiliza a opção ON DELETE CASCADE
CREATE TABLE Filho (
 ID_Filho SMALLINT AUTO_INCREMENT PRIMARY KEY,
 Nome_Filho VARCHAR(50),
 ID_Pai SMALLINT,
 FOREIGN KEY filho(ID_Pai) REFERENCES Pai(ID_Pai)
 ON DELETE CASCADE
 ON UPDATE CASCADE
);
```

**2. Como inserir dados nas tabelas "Pai" e "Filho" para testar a funcionalidade da chave estrangeira?**

```sql
-- Inserção de dados na tabela "Pai"
INSERT INTO Pai
VALUES (1,'João'), (2,'Mário'), (3,'Renato'), (4,'Emerson'), (5,'André');

-- Inserção de dados na tabela "Filho" relacionando-os com os pais
INSERT INTO Filho (Nome_Filho, ID_Pai)
VALUES ('João',1), ('Mário',1), ('Renato',3), ('Emerson',4), ('André',3);
```

**3. Como realizar uma consulta para mostrar os registros relacionados entre as tabelas "Pai" e "Filho"?**

```sql
-- Consulta para mostrar os registros relacionados
SELECT P.ID_Pai, P.Nome_Pai, F.ID_Filho, F.Nome_Filho
FROM Filho F
INNER JOIN Pai P
ON F.ID_Pai = P.ID_Pai;
```

**4. Como deletar um filho chamado "Renato" e resolver o erro "Error Code: 1175"?**

```sql
-- Tentativa de exclusão do filho "Renato" (Irá resultar em erro)
DELETE FROM Filho
WHERE Nome_Filho = 'Renato';

-- Solução 1: Desativar temporariamente o modo de atualização segura
SET SQL_SAFE_UPDATES = 0;

-- Após desativar o modo seguro, você pode executar a instrução DELETE novamente
DELETE FROM Filho
WHERE Nome_Filho = 'Renato';

-- Solução 2: Usar uma cláusula LIMIT para excluir um registro de cada vez
DELETE FROM Filho
WHERE Nome_Filho = 'Renato'
LIMIT 1;
```

**5. Como verificar se a exclusão cascateada funciona após excluir o pai "Renato"?**

```sql
-- Exclusão do pai "Renato" da tabela de pais
DELETE FROM Pai
WHERE Nome_Pai = 'Renato';

-- Verificação da exclusão cascateada do filho
SELECT * FROM Filho;
```

**6. Como criar uma tabela "Filho" que define o campo "ID_Pai" como NULL ao excluir um pai da tabela "Pai"?**

```sql
-- Exclusão das tabelas existentes
DROP TABLE Filho;
DROP TABLE Pai;

-- Criação da tabela "Pai" com chave primária ID_Pai
CREATE TABLE Pai (
 ID_Pai SMALLINT PRIMARY KEY,
 Nome_Pai VARCHAR(50)
) Engine=InnoDB;

-- Criação da tabela "Filho" com chave estrangeira que utiliza a opção ON DELETE SET NULL
CREATE TABLE Filho (
 ID_Filho SMALLINT AUTO_INCREMENT PRIMARY KEY,
 Nome_Filho VARCHAR(50),
 ID_Pai SMALLINT,
 FOREIGN KEY (ID_Pai) REFERENCES Pai(ID_Pai)
 ON DELETE SET NULL
 ON UPDATE CASCADE
) Engine=InnoDB;
```

**7. Como inserir dados nas tabelas "Pai" e "Filho" com a nova configuração de chave estrangeira?**

```sql
-- Inserção de dados na tabela "Pai"
INSERT INTO Pai
VALUES (1,'João'), (2,'Mário'), (3,'Renato'), (4,'Emerson'), (5,'André');

-- Inserção de dados na tabela "Filho" relacionando-os com os pais
INSERT INTO Filho (Nome_Filho, ID_Pai)
VALUES ('João',1), ('Mário',1), ('Renato',3), ('Emerson',4), ('André',3);
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>