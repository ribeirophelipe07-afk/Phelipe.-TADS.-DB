Exercício A:

```sql
SELECT produto, valor, data_venda
FROM VENDAS
WHERE vendedor = 'Ana'
ORDER BY data_venda;
```



Exercício B:

```sql
SELECT SUM(valor) AS total_eletronicos
FROM VENDAS
WHERE categoria = 'Eletrônicos';
```



Exercício C:

```sql
SELECT produto, valor
FROM VENDAS
WHERE valor BETWEEN 200 AND 1000;
```



Exercício D(Desafio):

```sql
SELECT 
    vendedor,
    COUNT(*) AS qtd_vendas,
    SUM(valor) AS total_vendido
FROM VENDAS
GROUP BY vendedor
ORDER BY total_vendido DESC;

```