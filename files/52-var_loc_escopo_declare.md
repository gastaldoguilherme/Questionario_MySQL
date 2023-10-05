> **Variáveis Locais e Escopo em MySQL**      
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Como você declararia uma variável local chamada `nome` no MySQL, que armazenará um valor do tipo VARCHAR com um valor inicial "John"?

**Resposta 1:**
Você pode declarar a variável local `nome` da seguinte forma:

```sql
DECLARE nome VARCHAR(50) DEFAULT 'John';
```

Isso declara uma variável chamada `nome` do tipo VARCHAR com um valor inicial de "John".

**Pergunta 2:** Crie um procedimento armazenado chamado `exemplo_incremento` que declara uma variável local `contador` do tipo INT e a incrementa em 1. Em seguida, selecione o valor da variável após a incrementação.

**Resposta 2:**
Você pode criar o procedimento `exemplo_incremento` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE exemplo_incremento()
BEGIN
    DECLARE contador INT DEFAULT 0;
    SET contador = contador + 1;
    SELECT contador;
END //
DELIMITER ;
```

**Pergunta 3:** Como você chamaria o procedimento `exemplo_incremento` para obter o valor da variável `contador` após a incrementação?

**Resposta 3:**
Você pode chamar o procedimento `exemplo_incremento` da seguinte forma:

```sql
CALL exemplo_incremento();
```

Isso executará o procedimento e retornará o valor da variável `contador` após a incrementação.

**Pergunta 4:** Crie um procedimento armazenado chamado `calcular_media` que recebe três números como parâmetros (num1, num2, num3), declara uma variável local `media` do tipo DECIMAL e calcula a média dos números passados como parâmetros. Em seguida, selecione o valor da variável `media`.

**Resposta 4:**
Você pode criar o procedimento `calcular_media` da seguinte forma:

```sql
DELIMITER //
CREATE PROCEDURE calcular_media(IN num1 DECIMAL(10, 2), IN num2 DECIMAL(10, 2), IN num3 DECIMAL(10, 2))
BEGIN
    DECLARE media DECIMAL(10, 2) DEFAULT 0;
    SET media = (num1 + num2 + num3) / 3;
    SELECT media;
END //
DELIMITER ;
```

**Pergunta 5:** Como você chamaria o procedimento `calcular_media` para calcular a média dos números 10.5, 15.75 e 20.25?

**Resposta 5:**
Você pode chamar o procedimento `calcular_media` da seguinte forma:

```sql
CALL calcular_media(10.5, 15.75, 20.25);
```

Isso executará o procedimento com os números fornecidos e retornará a média calculada.


&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>