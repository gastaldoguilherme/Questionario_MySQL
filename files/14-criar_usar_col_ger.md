> **Criar e Usar Colunas Geradas**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;


1. **O que são colunas geradas (campos calculados) em uma tabela MySQL e como você definiria uma coluna gerada chamada "total" que calcula a soma de duas outras colunas "valor1" e "valor2" em uma tabela chamada "exemplo"?**

   ```sql
   CREATE TABLE exemplo (
       ID INT PRIMARY KEY AUTO_INCREMENT,
       valor1 INT,
       valor2 INT,
       total INT GENERATED ALWAYS AS (valor1 + valor2) STORED
   );
   ```

2. **Explique a diferença entre colunas geradas VIRTUAL e STORED em uma tabela MySQL.**

   Resposta: Colunas geradas VIRTUAL são calculadas dinamicamente quando são consultadas, e seus dados não são armazenados fisicamente na tabela. Colunas geradas STORED, por outro lado, são calculadas no momento da inserção ou atualização de dados e seus valores são armazenados na tabela.

3. **Como você criaria uma coluna gerada que calcula o preço total de uma compra em uma tabela chamada "compras" com colunas "quantidade" e "preco_unitario" usando uma fórmula em que o preço total é a multiplicação da quantidade pelo preço unitário?**

   ```sql
   CREATE TABLE compras (
       ID INT PRIMARY KEY AUTO_INCREMENT,
       quantidade INT,
       preco_unitario DECIMAL(8,2),
       preco_total DECIMAL(10,2) GENERATED ALWAYS AS (quantidade * preco_unitario) STORED
   );
   ```

4. **É possível criar uma coluna gerada que faça referência a outras colunas geradas na mesma tabela? Explique.**

   Resposta: Sim, é possível criar uma coluna gerada que faça referência a outras colunas geradas na mesma tabela, desde que essas colunas tenham sido definidas antes na definição da tabela.

5. **Quais são algumas das limitações das colunas geradas em tabelas MySQL em relação a restrições como NOT NULL, DEFAULT e FOREIGN KEY?**

   Resposta: As colunas geradas não podem ter a restrição NOT NULL aplicada, não podem ter dados inseridos por uma declaração INSERT e nem serem modificadas por um UPDATE. Além disso, não podem ser utilizadas com definições de restrição DEFAULT e FOREIGN KEY.

6. **Dentro de uma coluna gerada, é possível usar a opção AUTO_INCREMENT? Por quê?**

   Resposta: Não, não é possível usar a opção AUTO_INCREMENT em uma coluna gerada. Isso ocorre porque uma coluna gerada já é calculada automaticamente com base em expressões definidas, não havendo necessidade de especificar valores incrementais.



&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>