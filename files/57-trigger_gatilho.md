> **Trigger (Gatilho)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria um trigger em MySQL chamado "tr_atualizar_estoque" que é acionado após uma operação de atualização (UPDATE) na tabela "Produtos" e que atualiza o estoque total de produtos em uma tabela chamada "Estoque" com base na diferença entre a quantidade antiga e a quantidade nova do produto atualizado?

**Resposta 1:**
Você pode criar um trigger em MySQL chamado "tr_atualizar_estoque" da seguinte forma:

```sql
DELIMITER //
CREATE TRIGGER tr_atualizar_estoque AFTER UPDATE
ON Produtos FOR EACH ROW
BEGIN
    DECLARE diferenca INT;
    SET diferenca = NEW.quantidade - OLD.quantidade;
    UPDATE Estoque SET estoque_total = estoque_total + diferenca WHERE produto_id = NEW.produto_id;
END;
//
DELIMITER ;
```

Este trigger é acionado após uma operação de atualização na tabela "Produtos" e calcula a diferença entre a quantidade antiga e a quantidade nova do produto atualizado. Em seguida, ele atualiza a tabela "Estoque" com base na diferença calculada.

**Pergunta 2:** Como você criaria um trigger em MySQL chamado "tr_registro_log" que é acionado após qualquer operação de inserção, atualização ou exclusão (INSERT, UPDATE, DELETE) na tabela "Clientes" e registra os detalhes da operação em uma tabela de log chamada "Log_Clientes"?

**Resposta 2:**
Você pode criar um trigger em MySQL chamado "tr_registro_log" da seguinte forma:

```sql
DELIMITER //
CREATE TRIGGER tr_registro_log AFTER INSERT, UPDATE, DELETE
ON Clientes FOR EACH ROW
BEGIN
    DECLARE operacao VARCHAR(10);
    
    IF INSERTING THEN
        SET operacao = 'INSERT';
    ELSEIF UPDATING THEN
        SET operacao = 'UPDATE';
    ELSE
        SET operacao = 'DELETE';
    END IF;
    
    INSERT INTO Log_Clientes (operacao, cliente_id, data_registro)
    VALUES (operacao, OLD.cliente_id, NOW());
END;
//
DELIMITER ;
```

Este trigger é acionado após qualquer operação de inserção, atualização ou exclusão na tabela "Clientes". Ele determina a operação que foi realizada (INSERT, UPDATE ou DELETE) e registra os detalhes da operação na tabela de log "Log_Clientes" junto com a data de registro.

**Pergunta 3:** Como você criaria um trigger em MySQL chamado "tr_atualizar_media" que é acionado após qualquer operação de inserção ou exclusão (INSERT ou DELETE) na tabela "Notas" e recalcula a média das notas e atualiza a tabela "Media_Notas" com a nova média?

**Resposta 3:**
Você pode criar um trigger em MySQL chamado "tr_atualizar_media" da seguinte forma:

```sql
DELIMITER //
CREATE TRIGGER tr_atualizar_media AFTER INSERT, DELETE
ON Notas FOR EACH ROW
BEGIN
    DECLARE total_notas INT;
    DECLARE nova_media DECIMAL(5, 2);
    
    SELECT COUNT(*) INTO total_notas FROM Notas;
    
    IF total_notas > 0 THEN
        SELECT SUM(valor) / total_notas INTO nova_media FROM Notas;
    ELSE
        SET nova_media = 0.00;
    END IF;
    
    UPDATE Media_Notas SET media = nova_media;
END;
//
DELIMITER ;
```

Este trigger é acionado após qualquer operação de inserção ou exclusão na tabela "Notas". Ele calcula o total de notas na tabela e a nova média das notas. Em seguida, atualiza a tabela "Media_Notas" com a nova média calculada.

**Pergunta 4:** Como você criaria um trigger em MySQL chamado "tr_verificar_limite" que é acionado antes de uma operação de inserção (INSERT) na tabela "Pedidos" e verifica se o valor total do pedido não excede um limite definido (por exemplo, 1000) e impede a inserção se exceder?

**Resposta 4:**
Você pode criar um trigger em MySQL chamado "tr_verificar_limite" da seguinte forma:

```sql
DELIMITER //
CREATE TRIGGER tr_verificar_limite BEFORE INSERT
ON Pedidos FOR EACH ROW
BEGIN
    DECLARE limite DECIMAL(10, 2);
    
    SET limite = 1000.00; -- Defina o limite desejado
    
    IF NEW.valor_total > limite THEN
        SIGNAL SQLSTATE '45000'
        SET MESSAGE_TEXT = 'Valor total do pedido excede o limite permitido';
    END IF;
END;
//
DELIMITER ;
```

Este trigger é acionado antes de uma operação de inserção na tabela "Pedidos". Ele verifica se o valor total do pedido (armazenado no campo "valor_total") excede o limite definido (neste caso, 1000) e impede a inserção se o limite for excedido, gerando um erro com uma mensagem personalizada.

**Pergunta 5:** Como você criaria um trigger em MySQL chamado "tr_audit_log" que é acionado após qualquer operação de atualização (UPDATE) na tabela "Funcionarios" e registra os detalhes da operação (campo, valor antigo e novo valor) em uma tabela de log chamada "Audit_Log_Funcionarios"?

**Resposta 5:**
Você pode criar um trigger em MySQL chamado "tr_audit_log" da seguinte forma:

```sql
DELIMITER //
CREATE TRIGGER tr_audit_log AFTER UPDATE
ON Funcionarios FOR EACH ROW
BEGIN
    DECLARE campo_afetado VARCHAR(50);
    
    IF OLD.nome <> NEW.nome THEN
        SET campo_afetado = 'Nome';
        INSERT INTO Audit_Log_Funcionarios (campo_afetado, valor_antigo, valor_novo, data_registro)
        VALUES (campo_afetado, OLD.nome, NEW.nome, NOW());
    END IF;
    
    IF OLD.salario <> NEW.salario THEN
        SET campo_afetado = 'Salario';


        INSERT INTO Audit_Log_Funcionarios (campo_afetado, valor_antigo, valor_novo, data_registro)
        VALUES (campo_afetado, OLD.salario, NEW.salario, NOW());
    END IF;
    
    -- Adicione mais condições para outros campos, se necessário
END;
//
DELIMITER ;
```

Este trigger é acionado após qualquer operação de atualização na tabela "Funcionarios". Ele verifica as diferenças entre os valores antigos (OLD) e novos (NEW) para cada campo que você deseja auditar (por exemplo, "nome" e "salario") e registra os detalhes da operação na tabela de log "Audit_Log_Funcionarios". Adicione mais condições para outros campos, se necessário.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>