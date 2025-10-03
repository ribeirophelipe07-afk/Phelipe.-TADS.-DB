```sql
--Liste todos os produtos mais caros do que o produto mais barato da categoria "Eletrônicos".
select categoria, valor produto
 from vendas 
 where valor > (
    SELECT MIN (valor) 
    FROM vendas 
    WHERE categoria = 'Eletrônicos'
)
order by valor desc;

select * from vendas;

--Mostre o vendedor que realizou a maior venda registrada na tabela.
select vendedor, valor 
from vendas 
where valor = (
    select max (valor) 
    from vendas
);

--Liste as categorias que têm pelo menos um produto acima do preço médio geral.
select produto, valor 
from vendas
where valor > (
select AVG ( valor) from  vendas
);
```