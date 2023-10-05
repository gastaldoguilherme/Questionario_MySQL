> **Constraints (Restrições)**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;



**Constraints (Restrições):**

1. **O que são constraints (restrições) em SQL MySQL e qual é o seu propósito principal em uma tabela?**

   **Resposta:** As constraints são regras aplicadas às colunas de uma tabela no SQL MySQL. Seu propósito principal é limitar os tipos de dados que podem ser inseridos, garantindo a integridade dos dados armazenados na tabela.

2. **Quais são as principais constraints em SQL MySQL e quais são suas funções?**

   **Resposta:** As principais constraints em SQL MySQL são:
   - `NOT NULL`: Impõe que uma coluna não aceite valores NULL, garantindo que o campo sempre tenha um valor.
   - `UNIQUE`: Garante a unicidade dos valores em uma coluna ou conjunto de colunas, evitando duplicatas.
   - `PRIMARY KEY`: Identifica de forma única cada registro na tabela e impõe valores únicos na coluna de chave primária.
   - `FOREIGN KEY`: Cria relacionamentos entre tabelas, onde um campo aponta para uma chave primária em outra tabela.
   - `DEFAULT`: Insere um valor padrão especificado em uma coluna quando nenhum outro valor é fornecido durante a inserção de dados.

3. **Qual é a diferença entre as constraints `UNIQUE` e `PRIMARY KEY` em SQL MySQL?**

   **Resposta:** Tanto `UNIQUE` quanto `PRIMARY KEY` garantem a unicidade dos dados em uma coluna ou conjunto de colunas. No entanto, a diferença principal é que uma constraint `PRIMARY KEY` também serve para identificar de forma única cada registro na tabela, enquanto `UNIQUE` apenas garante a unicidade dos valores, mas não é usada para identificação exclusiva.

4. **Quantas constraints `PRIMARY KEY` uma tabela pode ter em SQL MySQL?**

   **Resposta:** Cada tabela em SQL MySQL deve ter apenas uma constraint `PRIMARY KEY`, que identifica de forma única os registros na tabela.

5. **Para que serve a constraint `FOREIGN KEY` em SQL MySQL e como ela é usada para criar relacionamentos entre tabelas?**

   **Resposta:** A constraint `FOREIGN KEY` é usada para criar relacionamentos entre tabelas em um banco de dados. Ela é usada em uma tabela para apontar para uma chave primária em outra tabela, estabelecendo uma ligação entre os dados das duas tabelas e permitindo consultas e operações relacionadas.

6. **O que a constraint `DEFAULT` faz em SQL MySQL e como é utilizada para definir valores padrão em uma coluna?**

   **Resposta:** A constraint `DEFAULT` é usada para inserir um valor padrão especificado em uma coluna quando nenhum outro valor é fornecido durante a inserção de dados. Isso garante que, se nenhum valor for especificado, o valor padrão será usado automaticamente para preencher a coluna.


&nbsp;
<div align="center">
   
[Retornar ao índice](/README.md)

</div>