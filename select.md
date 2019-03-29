## Select

#### Mostrar os registros por ordem de acordo com a coluna escolhida:
```
select * from cursos
order by nome;
```
#### Mostrar os registros por ordem de acordo com a coluna escolhida em ordem decrescente:
```
select * from cursos
order by nome desc;
```
#### Filtar quais colunas serão exibidas:
```
select nome, carga, ano from cursos
order by nome;
```
#### Filtrar por linha os registros que serão exibidos:
```
select * from cursos 
where ano = '2016'
order by nome;
```
#### Utilizar operadores relacionais para filtrar o result set:
```
select * from cursos
where ano <= 2015
order by nome;
```
####  Filtrar o result set através de um determinado intervalo:
```
select * from cursos
where ano between 2014 and 2016;
```
#### Usar um filtro especifico:
```
select * from cursos
where ano in (2014, 2016)
order by ano desc;
```
#### Combinar operadores lógicos com operadores relacionais:
* nesse exemplo será mostrado os registros com carga maior que 30 e total de aulas menou ou igual a 20.
```
select * from cursos
where carga > 30 and totaulas <= 20
order by totaulas;
```
#### Filtar os registros que comecem com uma determinada letra:
* não fumciona sem aspas simples, posso colocar % na frente para exibir as que terminam com P, posso colocar % no final para exibir s que terminam com P e também posso colocar P entre dois % para exibir qualquer registro que contenha a letra P. NOT LIKE exibe os registros que não contem o parâmetro escolhido.
```
select * from cursos
-> where nome like 'p%';
```

Ps. 
select distinct profissao from gafanhotos
-> order by profissao;
    • filtra os registros para não exibir repetições.

select count(*) from cursos;
    • mostra o numero de registros

ex.
select count(*) from cursos
-> where carga >= 40;
aqui será exibido a quantidade de cursos com carga maior ou igual à 40
select max(carga) from cursos;
    • exibe o registro de maior valor. 

select min(totaulas) from cursos;
    • exibe o registro com o menor valor de aulas da tabela

select sum(totaulas) from cursos
-> where ano = 2016;
    • faz a soma dos registros. Nesse caso foi soma o total de aulas dos cursos de 2016

select avg(totaulas) from cursos
-> where ano = 2016;
    • mostra a média dos registros. Foi feita a média do total de aulas dos cursos de 2016

select carga, count(nome) from cursos
-> group by carga;
    • é possível agrupar os registros que se repetem e fazer a contagem dos registros na coluna nome

select carga, count(*) from cursos
-> group by carga
-> having count(*) > 3;
    •  é possível fazer o agrupamento selecionando apenas os grupos que tenham mais de 3 registros.

select carga, count(*) from cursos
-> where ano > 2015
-> group by carga
-> having carga > (select avg(carga) from cursos);
    • nesse exemplo estou utilizando um select dentro de outro select

