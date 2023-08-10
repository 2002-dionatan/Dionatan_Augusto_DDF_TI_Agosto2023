# Case 5
No banco de dados da Dadosfera, temos uma tabela chamada "users_emails" contendo detalhes do usuário. Escreva uma consulta SQL que seleciona usuários que se cadastraram nos últimos 30 dias e envie um relatório com esses dados. Por favor, explique o que cada parte da consulta faz.

SELECT
    *

FROM
    users_emails

WHERE
    < date_field > BETWEEN DATE_SUB(NOW(), INTERVAL 30 DAY)
AND NOW();

-- Explicação de cada parte da consulta:

- SELECT * : seleciona todos os registros da tabela;

- FROM users_emails : de qual tabela os dados serão buscados, neste caso é a "users_emails";
- WHERE < date_field > BETWEEN DATE_SUB(NOW(), INTERVAL 30 DAY)
AND NOW(): diz respeito ao parâmetro que será utilizado para realizar a consulta, sendo que, neste caso, buscaremos o campo de data (<date_field>),  visando buscar os cadastros dos usuários entre (BETWEEN) a data atual (NOW()) e o intervalo anterior de 30 dias em relação a ela (INTERVAL 30 DAY) AND NOW()) através da função "DATE_SUB";

- Com a consulta, pode se obter estes dados e criar gráficos pelo Excel com eles, gerando assim um relatório, por exemplo.

* **Obs.**: Na cláusula WHERE considerei o campo de data como "<date_field>", pois não foi informada qual seria o nome desta coluna de datas da tabela "users_emails".