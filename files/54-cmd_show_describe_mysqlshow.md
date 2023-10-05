> **Comandos SHOW, DESCRIBE e mysqlshow**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você usaria o comando `SHOW DATABASES` para listar todos os bancos de dados presentes no sistema MySQL?

**Resposta 1:**
Você pode usar o comando `SHOW DATABASES` da seguinte forma:

```sql
SHOW DATABASES;
```

Isso listará todos os bancos de dados disponíveis no sistema MySQL.

**Pergunta 2:** Suponha que você deseja verificar as colunas de uma tabela chamada `clientes`. Como você usaria o comando `SHOW COLUMNS` para listar as colunas dessa tabela?

**Resposta 2:**
Você pode usar o comando `SHOW COLUMNS` da seguinte forma:

```sql
SHOW COLUMNS FROM clientes;
```

Isso listará as colunas da tabela `clientes`.

**Pergunta 3:** Como você usaria o comando `DESCRIBE` para obter informações sobre a estrutura da tabela `pedidos`?

**Resposta 3:**
Você pode usar o comando `DESCRIBE` da seguinte forma:

```sql
DESCRIBE pedidos;
```

Isso fornecerá informações sobre a estrutura da tabela `pedidos`.

**Pergunta 4:** Qual é o equivalente abreviado do comando `DESCRIBE` que pode ser usado para obter informações sobre a estrutura de uma tabela?

**Resposta 4:**
O equivalente abreviado do comando `DESCRIBE` é o comando `DESC`. Você pode usá-lo da seguinte forma:

```sql
DESC tabela;
```

**Pergunta 5:** Como você usaria o comando `mysqlshow` para ver as tabelas em um banco de dados chamado `empresa`?

**Resposta 5:**
Você pode usar o comando `mysqlshow` da seguinte forma para ver as tabelas em um banco de dados específico:

```bash
mysqlshow -u seu_usuario -p empresa
```

Isso exibirá as tabelas no banco de dados `empresa`.

**Pergunta 6:** Suponha que você deseja ver informações sobre uma coluna chamada `nome` em uma tabela chamada `produtos`. Como você usaria o comando `mysqlshow` para fazer isso?

**Resposta 6:**
Você pode usar o comando `mysqlshow` da seguinte forma para ver informações sobre a coluna `nome` em uma tabela específica:

```bash
mysqlshow -u seu_usuario -p nome_do_banco_de_dados tabela coluna
```

Substitua `seu_usuario`, `nome_do_banco_de_dados`, `tabela` e `coluna` pelos valores apropriados. Por exemplo:

```bash
mysqlshow -u root -p minha_base_de_dados produtos nome
```

Isso exibirá informações sobre a coluna `nome` na tabela `produtos`.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>