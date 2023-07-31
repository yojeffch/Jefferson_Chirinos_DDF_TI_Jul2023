Case 5: Consulta SQL para selecionar usuários que se cadastraram nos últimos 30 dias.
Para selecionar os usuários que se cadastraram nos últimos 30 dias na tabela "users_emails", podemos utilizar a seguinte consulta SQL:

sql
SELECT *
FROM users_emails
WHERE data_cadastro >= DATE_SUB(CURDATE(), INTERVAL 30 DAY);
Explicação da consulta:
SELECT *: Seleciona todas as colunas da tabela.

FROM users_emails: Especifica a tabela "users_emails" de onde os dados serão recuperados.

WHERE data_cadastro >= DATE_SUB(CURDATE(), INTERVAL 30 DAY): Estabelece uma condição para a coluna "data_cadastro", onde ela deve ser maior ou igual à data atual menos 30 dias (ou seja, nos últimos 30 dias).

Essa consulta retornará todos os registros da tabela "users_emails" onde a data de cadastro esteja dentro do intervalo dos últimos 30 dias.

Lembrando que a consulta acima pode ser adaptada de acordo com a estrutura exata da tabela "users_emails" e o nome correto da coluna de data de cadastro.