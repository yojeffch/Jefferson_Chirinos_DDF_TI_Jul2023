Case 5: Consulta SQL para selecionar usu�rios que se cadastraram nos �ltimos 30 dias.
Para selecionar os usu�rios que se cadastraram nos �ltimos 30 dias na tabela "users_emails", podemos utilizar a seguinte consulta SQL:

sql
SELECT *
FROM users_emails
WHERE data_cadastro >= DATE_SUB(CURDATE(), INTERVAL 30 DAY);
Explica��o da consulta:
SELECT *: Seleciona todas as colunas da tabela.

FROM users_emails: Especifica a tabela "users_emails" de onde os dados ser�o recuperados.

WHERE data_cadastro >= DATE_SUB(CURDATE(), INTERVAL 30 DAY): Estabelece uma condi��o para a coluna "data_cadastro", onde ela deve ser maior ou igual � data atual menos 30 dias (ou seja, nos �ltimos 30 dias).

Essa consulta retornar� todos os registros da tabela "users_emails" onde a data de cadastro esteja dentro do intervalo dos �ltimos 30 dias.

Lembrando que a consulta acima pode ser adaptada de acordo com a estrutura exata da tabela "users_emails" e o nome correto da coluna de data de cadastro.