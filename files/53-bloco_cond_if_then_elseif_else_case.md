> **Blocos Condicionais IF – THEN – ELSEIF – ELSE e CASE**      
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Crie um procedimento armazenado chamado `classificar_produto` que aceita dois parâmetros: `preco` do tipo DECIMAL e `quantidade_em_estoque` do tipo INT. O procedimento deve classificar o produto com base nas seguintes regras:

- Se o `preco` for maior ou igual a 100.00 e a `quantidade_em_estoque` for maior ou igual a 10, classifique o produto como "Produto Premium".
- Se o `preco` for maior ou igual a 50.00 e a `quantidade_em_estoque` for maior ou igual a 20, classifique o produto como "Produto Standard".
- Caso contrário, classifique o produto como "Produto Básico".

**Resposta 1:**
Você pode criar o procedimento `classificar_produto` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE classificar_produto(IN preco DECIMAL(10, 2), IN quantidade_em_estoque INT)
BEGIN
    DECLARE categoria_produto VARCHAR(50);
    
    IF preco >= 100.00 AND quantidade_em_estoque >= 10 THEN
        SET categoria_produto = 'Produto Premium';
    ELSEIF preco >= 50.00 AND quantidade_em_estoque >= 20 THEN
        SET categoria_produto = 'Produto Standard';
    ELSE
        SET categoria_produto = 'Produto Básico';
    END IF;
    
    SELECT categoria_produto;
END //
DELIMITER ;
```

**Pergunta 2:** Como você chamaria o procedimento `classificar_produto` para classificar um produto com preço de 120.00 e 15 unidades em estoque?

**Resposta 2:**
Você pode chamar o procedimento `classificar_produto` da seguinte forma:

```sql
CALL classificar_produto(120.00, 15);
```

Isso executará o procedimento com os parâmetros fornecidos e retornará a classificação do produto.

**Pergunta 3:** Crie um procedimento chamado `calcular_desconto_total` que aceita três parâmetros: `subtotal` do tipo DECIMAL, `percentual_desconto` do tipo DECIMAL e `valor_limite` do tipo DECIMAL. O procedimento deve calcular o desconto total com base nas seguintes regras:

- Se o `subtotal` for maior ou igual ao `valor_limite`, aplique o desconto definido pelo `percentual_desconto` ao `subtotal`.
- Caso contrário, não aplique desconto, e o desconto total é 0.00.

**Resposta 3:**
Você pode criar o procedimento `calcular_desconto_total` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_desconto_total(IN subtotal DECIMAL(10, 2), IN percentual_desconto DECIMAL(5, 2), IN valor_limite DECIMAL(10, 2))
BEGIN
    DECLARE desconto_total DECIMAL(10, 2);
    
    IF subtotal >= valor_limite THEN
        SET desconto_total = subtotal * (percentual_desconto / 100);
    ELSE
        SET desconto_total = 0.00;
    END IF;
    
    SELECT desconto_total;
END //
DELIMITER ;
```

**Pergunta 4:** Como você chamaria o procedimento `calcular_desconto_total` para calcular o desconto total de um subtotal de 150.00, com um desconto de 20% e um valor limite de 100.00?

**Resposta 4:**
Você pode chamar o procedimento `calcular_desconto_total` da seguinte forma:

```sql
CALL calcular_desconto_total(150.00, 20.00, 100.00);
```

Isso executará o procedimento com os parâmetros fornecidos e retornará o desconto total calculado.

**Pergunta 5:** Crie um procedimento chamado `classificar_pedido` que aceita dois parâmetros: `total_pedido` do tipo DECIMAL e `status_pedido` do tipo VARCHAR(50). O procedimento deve classificar o pedido com base nas seguintes regras:

- Se o `total_pedido` for maior ou igual a 500.00 e o `status_pedido` for "Aprovado", classifique o pedido como "Pedido Confirmado".
- Se o `total_pedido` for maior ou igual a 200.00 e o `status_pedido` for "Aprovado", classifique o pedido como "Pedido Em Processamento".
- Caso contrário, classifique o pedido como "Pedido Pendente".

**Resposta 5:**
Você pode criar o procedimento `classificar_pedido` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE classificar_pedido(IN total_pedido DECIMAL(10, 2), IN status_pedido VARCHAR(50))
BEGIN
    DECLARE status_classificado VARCHAR(50);
    
    IF total_pedido >= 500.00 AND status_pedido = 'Aprovado' THEN
        SET status_classificado = 'Pedido Confirmado';
    ELSEIF total_pedido >= 200.00 AND status_pedido = 'Aprovado' THEN
        SET status_classificado = 'Pedido Em Processamento';
    ELSE
        SET status_classificado = 'Pedido Pendente';
    END IF;
    
    SELECT status_classificado;
END //
DELIMITER ;
```

**Pergunta 6:** Como você chamaria o procedimento `classificar_pedido` para classificar um pedido com um total de 600.00 e status "Aprovado"?

**Resposta 6:**
Você pode chamar o procedimento `classificar_pedido` da seguinte forma:

```sql
CALL classificar_pedido(600.00, 'Aprovado');
```

**Pergunta 7:** Crie um procedimento armazenado chamado `classificar_funcionario` que aceita um parâmetro `salario` do tipo DECIMAL. O procedimento deve usar um bloco condicional CASE para classificar o funcionário com base em seu salário da seguinte forma:

- Se o `salario` for maior ou igual a 5000.00, o funcionário é classificado como "Gerente".
- Se o `salario` estiver entre 3000.00 (inclusive) e 4999.99 (inclusive), o funcionário é classificado como "Supervisor".
- Se o `salario` estiver entre 2000.00 (inclusive) e 2999.99 (inclusive), o funcionário é classificado como "Assistente".
- Caso contrário, o funcionário é classificado como "Estagiário".

**Resposta 7:**
Você pode criar o procedimento `classificar_funcionario` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE classificar_funcionario(IN salario DECIMAL(10, 2))
BEGIN
    DECLARE cargo_funcionario VARCHAR(50);
    
    CASE
        WHEN salario >= 5000.00 THEN
            SET cargo_funcionario = 'Gerente';
        WHEN salario BETWEEN 3000.00 AND 4999.99 THEN
            SET cargo_funcionario = 'Supervisor';
        WHEN salario BETWEEN 2000.00 AND 2999.99 THEN
            SET cargo_funcionario = 'Assistente';
        ELSE
            SET cargo_funcionario = 'Estagiário';
    END CASE;
    
    SELECT cargo_funcionario;
END //
DELIMITER ;
```

**Pergunta 8:** Como você chamaria o procedimento `classificar_funcionario` para classificar um funcionário com um salário de 3500.00?

**Resposta 8:**
Você pode chamar o procedimento `classificar_funcionario` da seguinte forma:

```sql
CALL classificar_funcionario(3500.00);
```

Isso executará o procedimento com o salário fornecido e retornará a classificação do funcionário.

**Pergunta 9:** Crie um procedimento chamado `calcular_desconto` que aceita um parâmetro `valor_compra` do tipo DECIMAL e `cupom_desconto` do tipo VARCHAR(20). O procedimento deve usar um bloco condicional CASE para calcular o desconto com base nas seguintes regras:

- Se o `cupom_desconto` for "DESC10" e o `valor_compra` for maior ou igual a 100.00, aplique um desconto de 10% ao `valor_compra`.
- Se o `cupom_desconto` for "DESC20" e o `valor_compra` for maior ou igual a 200.00, aplique um desconto de 20% ao `valor_compra`.
- Se o `cupom_desconto` for "DESC30" e o `valor_compra` for maior ou igual a 300.00, aplique um desconto de 30% ao `valor_compra`.
- Caso contrário, não aplique desconto, e o valor do desconto é 0.00.

**Resposta 9:**
Você pode criar o procedimento `calcular_desconto` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_desconto(IN valor_compra DECIMAL(10, 2), IN cupom_desconto VARCHAR(20))
BEGIN
    DECLARE valor_desconto DECIMAL(10, 2);
    
    CASE
        WHEN cupom_desconto = 'DESC10' AND valor_compra >= 100.00 THEN
            SET valor_desconto = valor_compra * 0.10;
        WHEN cupom_desconto = 'DESC20' AND valor_compra >= 200.00 THEN
            SET valor_desconto = valor_compra * 0.20;
        WHEN cupom_desconto = 'DESC30' AND valor_compra >= 300.00 THEN
            SET valor_desconto = valor_compra * 0.30;
        ELSE
            SET valor_desconto = 0.00;
    END CASE;
    
    SELECT valor_desconto;
END //
DELIMITER ;
```

**Pergunta 10:** Como você chamaria o procedimento `calcular_desconto` para calcular o desconto de uma compra no valor de 250.00 com o cupom "DESC20"?

**Resposta 10:**
Você pode chamar o procedimento `calcular_desconto` da seguinte forma:

```sql
CALL calcular_desconto(250.00, 'DESC20');
```

Isso executará o procedimento com os parâmetros fornecidos e retornará o valor do desconto calculado.

**Pergunta 11:** Crie um procedimento chamado `avaliar_pedido` que aceita dois parâmetros: `total_pedido` do tipo DECIMAL e `status_pedido` do tipo VARCHAR(50). O procedimento deve usar um blo

co condicional CASE para avaliar o pedido com base nas seguintes regras:

- Se o `total_pedido` for maior ou igual a 1000.00 e o `status_pedido` for "Aprovado", avalie o pedido como "Pedido de Alto Valor Aprovado".
- Se o `total_pedido` for maior ou igual a 500.00 e o `status_pedido` for "Aprovado", avalie o pedido como "Pedido de Valor Médio Aprovado".
- Se o `status_pedido` for "Aprovado", avalie o pedido como "Pedido Aprovado, mas de Valor Baixo".
- Caso contrário, avalie o pedido como "Pedido Pendente".

**Resposta 11:**
Você pode criar o procedimento `avaliar_pedido` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE avaliar_pedido(IN total_pedido DECIMAL(10, 2), IN status_pedido VARCHAR(50))
BEGIN
    DECLARE avaliacao_pedido VARCHAR(100);
    
    CASE
        WHEN total_pedido >= 1000.00 AND status_pedido = 'Aprovado' THEN
            SET avaliacao_pedido = 'Pedido de Alto Valor Aprovado';
        WHEN total_pedido >= 500.00 AND status_pedido = 'Aprovado' THEN
            SET avaliacao_pedido = 'Pedido de Valor Médio Aprovado';
        WHEN status_pedido = 'Aprovado' THEN
            SET avaliacao_pedido = 'Pedido Aprovado, mas de Valor Baixo';
        ELSE
            SET avaliacao_pedido = 'Pedido Pendente';
    END CASE;
    
    SELECT avaliacao_pedido;
END //
DELIMITER ;
```

**Pergunta 12:** Como você chamaria o procedimento `avaliar_pedido` para avaliar um pedido com um total de 1200.00 e status "Aprovado"?

**Resposta 12:**
Você pode chamar o procedimento `avaliar_pedido` da seguinte forma:

```sql
CALL avaliar_pedido(1200.00, 'Aprovado');
```

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>