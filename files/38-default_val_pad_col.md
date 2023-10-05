> **Constraint DEFAULT – Valores padrão em colunas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria uma nova tabela chamada `clientes` com as colunas `id_cliente`, `nome`, `email`, onde a coluna `email` tem um valor padrão de "sememail@email.com"?

**Resposta 1:**
```sql
CREATE TABLE clientes
(
  id_cliente INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(255),
  email VARCHAR(255) DEFAULT 'sememail@email.com'
);
```

**Pergunta 2:** Como você modificaria uma tabela existente chamada `produtos` para que a coluna `quantidade_em_estoque` tenha um valor padrão de 0?

**Resposta 2:**
```sql
ALTER TABLE produtos
MODIFY COLUMN quantidade_em_estoque INT DEFAULT 0;
```

**Pergunta 3:** Suponha que você tenha uma tabela chamada `pedidos` com uma coluna chamada `status` que registra o status atual de um pedido. Como você definiria um valor padrão de "pendente" para a coluna `status`?

**Resposta 3:**
```sql
ALTER TABLE pedidos
MODIFY COLUMN status VARCHAR(255) DEFAULT 'pendente';
```

**Pergunta 4:** Como você removeria o valor padrão da coluna `telefone` em uma tabela chamada `contatos`?

**Resposta 4:**
```sql
ALTER TABLE contatos
MODIFY COLUMN telefone VARCHAR(20);
```

**Pergunta 5:** Suponha que você tenha uma tabela chamada `eventos` com uma coluna chamada `data` que armazena a data de um evento. Como você definiria um valor padrão de "2023-12-31" para a coluna `data`?

**Resposta 5:**
```sql
ALTER TABLE eventos
MODIFY COLUMN data DATE DEFAULT '2023-12-31';
```


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>