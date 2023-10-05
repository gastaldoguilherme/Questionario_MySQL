> **Carregar Dados Arquivo CSV**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



1. **Como você carregaria os dados de um arquivo CSV chamado "livros.csv" na tabela "tbl_livros" no banco de dados MySQL, onde os campos do arquivo CSV correspondem diretamente às colunas da tabela?**

```sql
LOAD DATA INFILE 'C:\\caminho\\para\\livros.csv'
INTO TABLE tbl_livros
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

2. **Suponha que você tenha um arquivo CSV com campos adicionais que não correspondem às colunas da tabela. Como você carregaria os dados relevantes e ignoraria os campos extras durante o carregamento?**

```sql
LOAD DATA INFILE 'C:\\caminho\\para\\dados.csv'
INTO TABLE tbl_dados
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
(@ignore, Coluna1, Coluna2, @ignore)
IGNORE 1 ROWS;
```

3. **Você deseja carregar dados de um arquivo CSV onde os campos são delimitados por ponto e vírgula (;) e as linhas são delimitadas por quebras de linha. Como você faria isso na declaração LOAD DATA INFILE?**

```sql
LOAD DATA INFILE 'C:\\caminho\\para\\arquivo.csv'
INTO TABLE tbl_exemplo
FIELDS TERMINATED BY ';'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

4. **O que acontece se você tentar carregar dados de um arquivo CSV que não está no diretório permitido pelo MySQL devido à configuração --secure-file-priv? Como você resolveria esse problema?**

Resposta: Se o arquivo CSV não estiver no diretório permitido pelo MySQL, você receberá um erro ao tentar usar a instrução LOAD DATA INFILE. Para resolver esse problema, você pode mover o arquivo para o diretório permitido conforme especificado na configuração --secure-file-priv. Certifique-se de que o MySQL tenha permissão para acessar o arquivo. Certifique-se também de que o arquivo esteja no formato correto e que as permissões de leitura estejam configuradas corretamente.

5. **Suponha que você deseja carregar dados de um arquivo CSV em uma tabela e, ao mesmo tempo, realizar alguma transformação nos dados antes de inseri-los na tabela (por exemplo, converter texto em maiúsculas). Como você faria isso usando o comando LOAD DATA INFILE?**

Resposta: Você pode usar o recurso SET para realizar transformações nos dados antes de inseri-los na tabela. Por exemplo:

```sql
LOAD DATA INFILE 'C:\\caminho\\para\\arquivo.csv'
INTO TABLE tbl_transformada
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
(@coluna1, @coluna2)
SET Coluna1 = UPPER(@coluna1), Coluna2 = UPPER(@coluna2);
```

Isso converterá os valores das colunas 1 e 2 em maiúsculas antes de inseri-los na tabela.

Espero que essas perguntas práticas e avançadas ajudem você a compreender melhor como carregar dados de arquivos CSV em tabelas MySQL usando o comando LOAD DATA INFILE.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>