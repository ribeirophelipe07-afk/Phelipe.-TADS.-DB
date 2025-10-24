SELECT
    c.nome AS cliente,
    v.produto
FROM Clientes c
LEFT JOIN VENDAS v
    ON c.id_cliente = v.id_cliente;

        SELECT
    NVL(c.nome, 'Sem Cliente') AS cliente,
    v.produto,
    v.valor
    FROM CLIENTES c
    RIGHT JOIN VENDAS v
    ON c.id_cliente = v.id_cliente;

        SELECT
    c.nome,
    c.cidade
FROM CLIENTES c
LEFT JOIN VENDAS v
    ON c.id_cliente = v.id_cliente
WHERE v.id IS NULL;

SELECT
    c.cidade,
    NVL(SUM(v.valor), 0) AS total_vendas
FROM CLIENTES c
LEFT JOIN VENDAS v
    ON c.id_cliente = v.id_cliente
GROUP BY c.cidade;



