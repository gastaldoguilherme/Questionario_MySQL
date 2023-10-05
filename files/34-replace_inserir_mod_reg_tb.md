> **REPLACE - Inserir ou Modificar Registro em Tabela**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você usaria a declaração `REPLACE` para adicionar um novo registro na tabela `paises` com o país "Angola" e a capital "Luanda"?

**Resposta 1:**
```sql
REPLACE INTO paises(nome_Pais, nome_Capital)
VALUES ('Angola', 'Luanda');
```

**Pergunta 2:** Suponha que você tenha uma tabela chamada `clientes` com colunas `ID_Cliente`, `Nome` e `Email`, e você deseja atualizar o email do cliente com `ID_Cliente` igual a 101 para "novonome@email.com". Como você faria isso usando a declaração `REPLACE`?

**Resposta 2:**
```sql
REPLACE INTO clientes(ID_Cliente, Email)
VALUES (101, 'novonome@email.com');
```

**Pergunta 3:** Qual é a principal diferença entre a declaração `REPLACE` e a declaração `INSERT` em relação à inserção de novos registros?

**Resposta 3:** A principal diferença é que a declaração `REPLACE` verifica se um registro com os mesmos valores de chave primária ou coluna com restrição `UNIQUE` já existe na tabela. Se existir, ela atualiza os valores existentes; caso contrário, insere um novo registro. A declaração `INSERT`, por outro lado, sempre insere um novo registro e gera um erro se houver um conflito com valores de chave primária ou restrição `UNIQUE`.

**Pergunta 4:** Suponha que você tenha uma tabela chamada `produtos` com colunas `ID_Produto`, `Nome` e `Preco`, e deseja adicionar um novo produto chamado "ProdutoX" com preço de 19.99. Como você faria isso usando a declaração `REPLACE`?

**Resposta 4:**
```sql
REPLACE INTO produtos(Nome, Preco)
VALUES ('ProdutoX', 19.99);
```

**Pergunta 5:** Se você tentar usar a declaração `REPLACE` em uma tabela que não possui uma chave primária ou coluna com restrição `UNIQUE`, qual será o comportamento da declaração?

**Resposta 5:** Se a tabela não tiver uma chave primária ou coluna com restrição `UNIQUE`, a declaração `REPLACE` funcionará como uma declaração `INSERT` comum. Ela sempre inserirá um novo registro, independentemente da existência de registros semelhantes na tabela.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>