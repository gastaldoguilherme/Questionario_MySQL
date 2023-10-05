> **Chave Primária (Primary Key)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



**1. O que é uma chave primária (Primary Key) em um banco de dados relacional e quais são suas principais características?**

   - Resposta: Uma chave primária é um campo ou conjunto de campos em uma tabela que é usado para identificar de forma única e exclusiva cada linha na tabela. Ela não permite repetição de valores nas linhas e não pode conter valores nulos.

**2. Quais são os dois tipos principais de chave primária mencionados no texto?**

   - Resposta: Os dois tipos principais de chave primária são "Simples" e "Composta".

**3. Como é definida uma chave primária simples e quando ela é usada?**

   - Resposta: Uma chave primária simples é constituída por apenas uma coluna em uma tabela. É usada quando não existe um campo "natural" que possa ser usado como chave primária.

**4. O que é uma Chave Surrogada ou Substituta?**

   - Resposta: Uma Chave Surrogada ou Substituta é um valor numérico único adicionado à tabela para servir como chave primária quando não há um campo "natural" disponível para essa finalidade. Ela não possui significado para os usuários.

**5. Como criar uma chave primária em uma nova tabela no MySQL usando o Modo 1 - Constraint em Nível de Coluna?**

   - Resposta: Você pode criar uma chave primária em uma nova tabela no MySQL usando o Modo 1 - Constraint em Nível de Coluna da seguinte forma:

```sql
CREATE TABLE funcionarios (
  id_func smallint PRIMARY KEY AUTO_INCREMENT,
  nome_func VARCHAR(30) NOT NULL,
  sobrenome_func VARCHAR(50) NOT NULL
);
```

**6. Como criar uma chave primária em uma nova tabela no MySQL usando o Modo 2 - Constraint em Nível de Tabela (Nomeada)?**

   - Resposta: Você pode criar uma chave primária em uma nova tabela no MySQL usando o Modo 2 - Constraint em Nível de Tabela (Nomeada) da seguinte forma:

```sql
CREATE TABLE departamentos_mod (
  id_dep smallint AUTO_INCREMENT,
  nome_dep VARCHAR(30) NOT NULL,
  PRIMARY KEY(id_dep)
);
```

**7. Como adicionar uma chave primária a uma tabela existente no MySQL?**

   - Resposta: Você pode adicionar uma chave primária a uma tabela existente no MySQL da seguinte maneira:

```sql
ALTER TABLE fornecedores
ADD PRIMARY KEY (id_forn);
```

**8. Como criar uma chave primária composta que englobe duas colunas em uma nova tabela no MySQL?**

   - Resposta: Você pode criar uma chave primária composta em uma nova tabela no MySQL da seguinte forma:

```sql
CREATE TABLE vendas (
  id_produto smallint,
  id_cliente smallint,
  qtde smallint,
  PRIMARY KEY(id_produto, id_cliente)
);
```
&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
