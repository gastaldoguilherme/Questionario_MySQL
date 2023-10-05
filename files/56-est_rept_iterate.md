> **Estruturas de Repetição – ITERATE**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


**Pergunta 1:** Como você usaria a declaração `ITERATE` em conjunto com uma estrutura de repetição `LOOP` para calcular a soma dos números de 1 a 100, pulando os números múltiplos de 5, e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 1:**
Você pode usar a declaração `ITERATE` em conjunto com uma estrutura de repetição `LOOP` para calcular a soma dos números de 1 a 100, pulando os números múltiplos de 5, da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_soma_sem_multiplos_de_5()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma INT DEFAULT 0;
    loop_teste: LOOP
        SET contador = contador + 1;
        IF contador % 5 = 0 THEN
            ITERATE loop_teste; -- Pula múltiplos de 5
        END IF;
        SET soma = soma + contador;
        IF contador >= 100 THEN
            LEAVE loop_teste;
        END IF;
    END LOOP loop_teste;
    SELECT soma;
END //
DELIMITER ;

-- Testando o procedimento
CALL calcular_soma_sem_multiplos_de_5();
```

Isso calculará a soma dos números de 1 a 100, pulando os múltiplos de 5 usando a declaração `ITERATE` para pular esses números e retornará o resultado.

**Pergunta 2:** Como você usaria a declaração `ITERATE` em conjunto com uma estrutura de repetição `REPEAT` para calcular a soma dos números pares de 2 a 50 e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 2:**
Você pode usar a declaração `ITERATE` em conjunto com uma estrutura de repetição `REPEAT` para calcular a soma dos números pares de 2 a 50 da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_soma_numeros_pares()
BEGIN
    DECLARE contador INT DEFAULT 2;
    DECLARE soma INT DEFAULT 0;
    REPEAT
        SET soma = soma + contador;
        SET contador = contador + 2; -- Incrementa para o próximo número par
    UNTIL contador > 50;
    SELECT soma;
END //
DELIMITER ;

-- Testando o procedimento
CALL calcular_soma_numeros_pares();
```

Isso calculará a soma dos números pares de 2 a 50 usando a declaração `ITERATE` para pular para o próximo número par a cada iteração e retornará o resultado.

**Pergunta 3:** Como você usaria a declaração `ITERATE` em conjunto com uma estrutura de repetição `WHILE` para exibir os números de 1 a 20, pulando os números divisíveis por 3, em um procedimento armazenado MySQL?

**Resposta 3:**
Você pode usar a declaração `ITERATE` em conjunto com uma estrutura de repetição `WHILE` para exibir os números de 1 a 20, pulando os números divisíveis por 3, da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE mostrar_numeros_sem_divisiveis_por_3()
BEGIN
    DECLARE contador INT DEFAULT 0;
    WHILE contador < 20 DO
        SET contador = contador + 1;
        IF contador % 3 = 0 THEN
            ITERATE; -- Pula números divisíveis por 3
        END IF;
        SELECT contador;
    END WHILE;
END //
DELIMITER ;

-- Testando o procedimento
CALL mostrar_numeros_sem_divisiveis_por_3();
```

Isso exibirá os números de 1 a 20, pulando os números divisíveis por 3 usando a declaração `ITERATE` para pular esses números.

**Pergunta 4:** Como você usaria a declaração `ITERATE` em conjunto com uma estrutura de repetição `LOOP` para calcular a média dos números de 1 a 100, excluindo os números ímpares, e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 4:**
Você pode usar a declaração `ITERATE` em conjunto com uma estrutura de repetição `LOOP` para calcular a média dos números de 1 a 100, excluindo os números ímpares, da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_media_sem_impares()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma INT DEFAULT 0;
    DECLARE quantidade INT DEFAULT 0;
    loop_teste: LOOP
        SET contador = contador + 1;
        IF contador % 2 <> 0 THEN
            ITERATE loop_teste; -- Pula números ímpares
        END IF;
        SET soma = soma + contador;
        SET quantidade = quantidade + 1;
        IF contador >= 100 THEN
            LEAVE loop_teste;
        END IF;
    END LOOP loop_teste;
    SELECT soma / quantidade AS media;
END //
DELIMITER ;

-- Testando o procedimento
CALL calcular_media_sem_impares();
```

Isso calculará a média dos números de 1 a 100, excluindo os números ímpares, usando a declaração `ITERATE` para pular os números ímpares e retornará o resultado.

**Pergunta 5:** Como você usaria a declaração `ITERATE` em conjunto com uma estrutura de repetição `REPEAT` para calcular a soma dos quadrados dos números de 1 a 10 e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 5:**
Você pode usar a declaração `ITERATE` em conjunto com uma estrutura de repetição `REPEAT` para calcular a soma dos quadrados dos números de 1 a 10 da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_soma_quadrados()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma_quadrados INT DEFAULT 0;
    REPEAT
        SET contador = contador + 1;
        SET soma_quadrados = soma_quadrados + (contador * contador);
    UNTIL contador >= 10;
    SELECT soma_quadrados;
END //

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>