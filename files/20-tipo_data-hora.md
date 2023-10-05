> **Data e Hora**     
> Repositório: Banco de Dados MySQL - Fundamentos  
> GitHub: @gastaldoguilherme

&nbsp;

**Pergunta 1:** Crie uma tabela chamada "eventos" que armazene informações sobre eventos futuros, incluindo o nome do evento, a data e hora do evento (use o tipo DATETIME), e um ID exclusivo para cada evento.

**Resposta 1:**
```sql
-- Criar a tabela "eventos"
CREATE TABLE eventos (
  idEvento INT PRIMARY KEY AUTO_INCREMENT,
  nomeEvento VARCHAR(100),
  dataHoraEvento DATETIME
);
```

**Pergunta 2:** Insira três registros na tabela "eventos" com informações sobre eventos futuros, incluindo o nome e a data e hora de cada evento.

**Resposta 2:**
```sql
-- Inserir registros na tabela "eventos"
INSERT INTO eventos (nomeEvento, dataHoraEvento)
VALUES
('Evento A', '2023-06-15 10:00:00'),
('Evento B', '2023-07-20 15:30:00'),
('Evento C', '2023-08-10 19:45:00');
```

**Pergunta 3:** Consulte a tabela "eventos" para obter os eventos que ocorrerão após "2023-07-01 00:00:00".

**Resposta 3:**
```sql
-- Consultar eventos que ocorrerão após "2023-07-01 00:00:00"
SELECT * FROM eventos
WHERE dataHoraEvento > '2023-07-01 00:00:00';
```

**Pergunta 4:** Crie uma tabela chamada "lembretes" para armazenar lembretes diários, incluindo o texto do lembrete e a hora do dia em que o lembrete deve ser exibido (use o tipo TIME).

**Resposta 4:**
```sql
-- Criar a tabela "lembretes"
CREATE TABLE lembretes (
  idLembrete INT PRIMARY KEY AUTO_INCREMENT,
  textoLembrete TEXT,
  horaExibicao TIME
);
```

**Pergunta 5:** Insira um lembrete na tabela "lembretes" com o texto "Reunião de Equipe" para ser exibido às 09:30 da manhã.

**Resposta 5:**
```sql
-- Inserir um lembrete na tabela "lembretes"
INSERT INTO lembretes (textoLembrete, horaExibicao)
VALUES ('Reunião de Equipe', '09:30:00');
```

**Pergunta 6:** Consulte a tabela "lembretes" para obter todos os lembretes que devem ser exibidos após as 10:00 da manhã.

**Resposta 6:**
```sql
-- Consultar lembretes que devem ser exibidos após as 10:00 da manhã
SELECT * FROM lembretes
WHERE horaExibicao > '10:00:00';
```

Essas perguntas e respostas fornecem exemplos de como trabalhar com data e hora no MySQL, incluindo a criação de tabelas, inserção de registros e consultas com base em critérios de data e hora.

&nbsp;    

<div align="center">
   
[Retornar ao índice](/README.md)

</div>