> **Função para Capitalizar a Inicial de uma Frase ou Palavra**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você criaria uma função armazenada no MySQL que converte a primeira letra de uma palavra ou frase para maiúscula?

**Resposta 1:**
Para criar uma função armazenada no MySQL que converte a primeira letra de uma palavra ou frase para maiúscula, você pode usar o seguinte código SQL:

```sql
DROP FUNCTION IF EXISTS inicial_maiuscula;
DELIMITER //
CREATE FUNCTION inicial_maiuscula(texto VARCHAR(100))
RETURNS VARCHAR(100)
BEGIN
    RETURN CONCAT(UPPER(LEFT(texto, 1)), SUBSTRING(texto, 2));
END //
DELIMITER ;
```

**Pergunta 2:** Como você usaria a função `inicial_maiuscula` para converter a primeira letra de uma palavra ou frase em maiúscula?

**Resposta 2:**
Você pode usar a função `inicial_maiuscula` em uma consulta SQL da seguinte maneira:

```sql
SELECT inicial_maiuscula('exemplo de texto com letra minúscula');
```

Isso retornará a primeira letra da frase em maiúscula e manterá o restante do texto como está.

**Pergunta 3:** Como você usaria a função `inicial_maiuscula` em uma consulta SQL para capitalizar a primeira letra do nome "maria"?

**Resposta 3:**
Você pode usar a função `inicial_maiuscula` em uma consulta SQL da seguinte maneira para capitalizar a primeira letra do nome "maria":

```sql
SELECT inicial_maiuscula('maria');
```

Isso retornará "Maria" com a primeira letra em maiúscula.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>