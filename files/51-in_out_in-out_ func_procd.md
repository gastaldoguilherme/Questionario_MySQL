> **Funções e Procedimentos Armazenados - Parâmetros IN, OUT e INOUT**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria uma função armazenada no MySQL chamada `consultar_cliente` que recebe o ID de um cliente como entrada (parâmetro IN) e retorna todos os detalhes desse cliente?

**Resposta 1:**
Você pode criar a função `consultar_cliente` da seguinte maneira:

```sql
CREATE FUNCTION consultar_cliente(IN id_cliente INT)
RETURNS TABLE
BEGIN
    RETURN (SELECT * FROM clientes WHERE id = id_cliente);
END;
```

**Pergunta 2:** Como você chamaria a função `consultar_cliente` para obter todos os detalhes do cliente com ID 1?

**Resposta 2:**
Você pode chamar a função `consultar_cliente` da seguinte forma:

```sql
SELECT * FROM consultar_cliente(1);
```

Isso retornará todos os detalhes do cliente com ID 1.

**Pergunta 3:** Como você criaria um procedimento armazenado no MySQL chamado `calcular_media_precos` que calcula a média de preços de produtos e a retorna como saída (parâmetro OUT)?

**Resposta 3:**
Você pode criar o procedimento `calcular_media_precos` da seguinte maneira:

```sql
CREATE PROCEDURE calcular_media_precos(OUT media DECIMAL(10, 2))
BEGIN
    SELECT AVG(preco) INTO media FROM produtos;
END;
```

**Pergunta 4:** Como você chamaria o procedimento `calcular_media_precos` para calcular a média de preços dos produtos e obter o resultado?

**Resposta 4:**
Você pode chamar o procedimento `calcular_media_precos` da seguinte forma:

```sql
DECLARE @media DECIMAL(10, 2);
CALL calcular_media_precos(@media);
SELECT @media;
```

Isso calculará a média de preços dos produtos e armazenará o resultado em `@media`, que pode ser posteriormente selecionado para exibição.

**Pergunta 5:** Como você criaria um procedimento armazenado no MySQL chamado `calcular_aumento_preco` que recebe o preço atual de um produto (parâmetro INOUT) e o percentual de aumento (parâmetro IN) e atualiza o preço do produto com o novo valor?

**Resposta 5:**
Você pode criar o procedimento `calcular_aumento_preco` da seguinte maneira:

```sql
CREATE PROCEDURE calcular_aumento_preco(INOUT preco_antigo DECIMAL(10, 2), IN percentual_aumento DECIMAL(5, 2))
BEGIN
    SET preco_antigo = preco_antigo * (1 + (percentual_aumento / 100));
END;
```

**Pergunta 6:** Como você chamaria o procedimento `calcular_aumento_preco` para aumentar o preço de um produto com um preço atual de 50.00 em 10%?

**Resposta 6:**
Você pode chamar o procedimento `calcular_aumento_preco` da seguinte forma:

```sql
DECLARE @preco DECIMAL(10, 2);
SET @preco = 50.00;
CALL calcular_aumento_preco(@preco, 10.00);
SELECT @preco;
```

Isso aumentará o preço do produto em 10% e retornará o novo preço em `@preco`.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>