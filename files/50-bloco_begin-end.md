> **Funções e Procedimentos Armazenados - Blocos BEGIN .. END**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você criaria uma função armazenada no MySQL chamada `calcular_salario_liquido` que recebe o salário bruto de um funcionário como entrada e calcula o salário líquido após deduções de impostos, onde a dedução de impostos é de 20% do salário bruto?

**Resposta 1:**
Você pode criar a função `calcular_salario_liquido` da seguinte maneira:

```sql
DELIMITER //
CREATE FUNCTION calcular_salario_liquido(salario_bruto DECIMAL(10, 2))
RETURNS DECIMAL(10, 2)
BEGIN
    DECLARE salario_liquido DECIMAL(10, 2);

    -- Cálculos
    SET salario_liquido = salario_bruto - (salario_bruto * 0.20); -- Dedução de 20% para impostos

    RETURN salario_liquido;
END //
DELIMITER ;
```

**Pergunta 2:** Como você chamaria a função `calcular_salario_liquido` para calcular o salário líquido de um funcionário com um salário bruto de 5000.00?

**Resposta 2:**
Você pode chamar a função `calcular_salario_liquido` da seguinte forma:

```sql
SELECT calcular_salario_liquido(5000.00);
```

Isso calculará o salário líquido para um salário bruto de 5000.00 e retornará o resultado.

**Pergunta 3:** Como você criaria um procedimento armazenado no MySQL chamado `atualizar_preco_produtos` que aumenta o preço de todos os produtos em uma tabela multiplicando-o por 1,1 (aumento de 10%)?

**Resposta 3:**
Você pode criar o procedimento `atualizar_preco_produtos` da seguinte maneira:

```sql
DELIMITER //
CREATE PROCEDURE atualizar_preco_produtos()
BEGIN
    UPDATE produtos
    SET preco = preco * 1.1; -- Aumento de 10%
END //
DELIMITER ;
```

**Pergunta 4:** Como você chamaria o procedimento `atualizar_preco_produtos` para aumentar os preços dos produtos na tabela?

**Resposta 4:**
Você pode chamar o procedimento `atualizar_preco_produtos` da seguinte forma:

```sql
CALL atualizar_preco_produtos();
```

Isso executará o procedimento e aumentará os preços dos produtos na tabela multiplicando-os por 1,1 (aumento de 10%).

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>