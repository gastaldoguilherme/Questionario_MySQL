> **Estruturas de Repetição: LOOP - REPEAT - WHILE**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você usaria a estrutura de repetição `LOOP` para calcular a soma dos números de 1 a 10 e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 1:**
Você pode usar a estrutura de repetição `LOOP` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_soma()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma INT DEFAULT 0;
    loop_teste: LOOP
        SET contador = contador + 1;
        SET soma = soma + contador;
        IF contador >= 10 THEN
            LEAVE loop_teste;
        END IF;
    END LOOP loop_teste;
    SELECT soma;
END //
DELIMITER ;

-- Testando o procedimento
CALL calcular_soma();
```

Isso calculará a soma dos números de 1 a 10 usando um loop `LOOP` e retornará o resultado.

**Pergunta 2:** Como você usaria a estrutura de repetição `REPEAT` para calcular a soma dos números de 1 a 10 e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 2:**
Você pode usar a estrutura de repetição `REPEAT` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_soma_repita()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma INT DEFAULT 0;
    REPEAT
        SET contador = contador + 1;
        SET soma = soma + contador;
    UNTIL contador >= 10
    END REPEAT;
    SELECT soma;
END //
DELIMITER ;

-- Testando o procedimento
CALL calcular_soma_repita();
```

Isso calculará a soma dos números de 1 a 10 usando um loop `REPEAT` e retornará o resultado.

**Pergunta 3:** Como você usaria a estrutura de repetição `WHILE` para calcular a soma dos números de 1 a 10 e retornar o resultado em um procedimento armazenado MySQL?

**Resposta 3:**
Você pode usar a estrutura de repetição `WHILE` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_soma_while()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma INT DEFAULT 0;
    WHILE contador < 10 DO
        SET contador = contador + 1;
        SET soma = soma + contador;
    END WHILE;
    SELECT soma;
END //
DELIMITER ;

-- Testando o procedimento
CALL calcular_soma_while();
```

Isso calculará a soma dos números de 1 a 10 usando um loop `WHILE` e retornará o resultado.

**Pergunta 4:** Como você pode resolver o problema de um loop `REPEAT` que incrementa a variável antes de verificar a condição, garantindo que o valor seja correto?

**Resposta 4:**
Você pode resolver o problema ajustando a estrutura do loop `REPEAT` e utilizando a cláusula `LEAVE` para sair do loop quando a condição não for mais satisfeita. Aqui está um exemplo:

```sql
DROP PROCEDURE IF EXISTS calcular_soma_repita;
DELIMITER //
CREATE PROCEDURE calcular_soma_repita_corrigido()
BEGIN
    DECLARE contador INT DEFAULT 0;
    DECLARE soma INT DEFAULT 0;
    IF contador >= 10 THEN
        SELECT 'O valor inicial do contador já atende à condição.' AS Mensagem;
        RETURN;
    END IF;
    REPEAT
        SET contador = contador + 1;
        SET soma = soma + contador;
    UNTIL contador >= 10
    END REPEAT;
    SELECT soma;
END //
DELIMITER ;

-- Testando o procedimento corrigido
CALL calcular_soma_repita_corrigido();
```

Agora, o loop `REPEAT` verifica primeiro se a condição é atendida antes de incrementar a variável, evitando resultados incorretos.

**Pergunta 5:** Como você usaria um rótulo em uma estrutura de repetição, como `LOOP`, `REPEAT` ou `WHILE`, em um procedimento armazenado MySQL?

**Resposta 5:**
Você pode usar um rótulo para identificar a estrutura de repetição e, posteriormente, usar a cláusula `LEAVE` com o rótulo para sair do loop quando necessário. Aqui está um exemplo usando o rótulo `loop_teste` em um loop `LOOP`:

```sql
DELIMITER //
CREATE PROCEDURE exemplo_com_rotulo()
BEGIN
    DECLARE contador INT DEFAULT 0;
    loop_teste: LOOP
        SET contador = contador + 1;
        IF contador >= 5 THEN
            LEAVE loop_teste;
        END IF;
    END LOOP loop_teste;
    SELECT contador;
END //
DELIMITER ;

-- Testando o procedimento com rótulo
CALL exemplo_com_rotulo();
```

Neste exemplo, o rótulo `loop_teste` é usado para identificar o loop `LOOP`, e a cláusula `LEAVE` é usada com o rótulo para sair do loop quando `contador` for maior ou igual a 5.

**Pergunta 6:** Como você usaria a estrutura de repetição `WHILE` para realizar um loop infinito em um procedimento armazenado MySQL?

**Resposta 6:**
Você pode criar um loop infinito usando a estrutura de repetição `WHILE` simplesmente fornecendo uma condição que sempre seja verdadeira. Por exemplo, para criar um loop infinito que exibe "Loop infinito" continuamente, você pode fazer o seguinte:

```sql
DELIMITER //
CREATE PROCEDURE loop_infinito()
BEGIN
    WHILE 1 DO
        SELECT 'Loop infinito' AS Mensagem;
    END WHILE;
END //
DELIMITER ;

-- Para interromper o loop infinito, você pode executar:
-- KILL [CONNECTION_ID];
```

Este procedimento armazenado usará um loop `WHILE` que sempre terá uma condição verdadeira (`1` é sempre verdadeiro), o que resultará em um loop infinito que continuará exibindo "Loop infinito" até ser interrompido manualmente com o comando `KILL` no MySQL.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>