> **Expressões Regulares (REGEXP)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você selecionaria todos os nomes de livros da tabela `livros` onde o nome do livro começa com uma vogal (ou seja, 'A', 'E', 'I', 'O' ou 'U')?

**Resposta 1:**
```sql
SELECT Nome_Livro
FROM livros
WHERE Nome_Livro REGEXP '^[AEIOU]';
```

**Pergunta 2:** Como você encontraria todos os registros da tabela `produtos` onde a descrição do produto inclui a palavra "tecnologia" em qualquer parte da string, independentemente de maiúsculas ou minúsculas?

**Resposta 2:**
```sql
SELECT *
FROM produtos
WHERE descricao_produto REGEXP '[Tt][Ee][Cc][Nn][Oo][Ll][Oo][Gg][Ii][Aa]';
```

**Pergunta 3:** Suponha que você tenha uma tabela chamada `emails` com coluna `endereco_email`. Como você selecionaria todos os registros onde o endereço de e-mail não segue o formato padrão de e-mail (por exemplo, não contém um "@" e um ".com")?

**Resposta 3:**
```sql
SELECT *
FROM emails
WHERE endereco_email NOT REGEXP '[@.].com';
```

**Pergunta 4:** Como você encontraria todos os nomes de cidades na tabela `cidades` que começam com uma letra maiúscula seguida de duas letras minúsculas?

**Resposta 4:**
```sql
SELECT Nome_Cidade
FROM cidades
WHERE Nome_Cidade REGEXP '^[A-Z][a-z][a-z]';
```

**Pergunta 5:** Como você selecionaria todos os registros da tabela `documentos` onde o número do documento possui exatamente 5 dígitos?

**Resposta 5:**
```sql
SELECT *
FROM documentos
WHERE numero_documento REGEXP '^[0-9]{5}$';
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>