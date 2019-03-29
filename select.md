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
#### Filtrar os registros que comecem com uma determinada letra:
* não fumciona sem aspas simples, posso colocar % na frente para exibir as que terminam com P, posso colocar % no final para exibir s que terminam com P e também posso colocar P entre dois % para exibir qualquer registro que contenha a letra P. NOT LIKE exibe os registros que não contem o parâmetro escolhido.
```
select * from cursos
-> where nome like 'p%';
```
#### Filtrar os registros para não exibir repetições:
```
select distinct profissao from gafanhotos
order by profissao;
``` 
#### Mostrar o numero de registros:
```
select count(*) from cursos;
``` 
#### Exemplo
* aqui será exibido a quantidade de cursos com carga maior ou igual à 40
```
select count(*) from cursos
where carga >= 40;
```
#### Exibir o registro de maior valor:
``` 
select max(carga) from cursos;
``` 
#### Exibir o registro com o menor valor de aulas da tabela:
```
select min(totaulas) from cursos;
```
#### Fazer a soma dos registros:
* Nesse caso foi feita a soma o total de aulas dos cursos de 2016
``` 
select sum(totaulas) from cursos
-> where ano = 2016;
```
#### Mostrar a média dos registros:
* Foi feita a média do total de aulas dos cursos de 2016
```  
select avg(totaulas) from cursos
where ano = 2016;
```
#### Agrupar os registros que se repetem e fazer a contagem dos registros na coluna nome:
```
select carga, count(nome) from cursos
group by carga;
```
#### Fazer o agrupamento selecionando apenas os grupos que tenham mais de 3 registros:
```   
select carga, count(*) from cursos
group by carga
having count(*) > 3;
```
#### Utilizar um select dentro de outro select:
```
select carga, count(*) from cursos
where ano > 2015
group by carga
having carga > (select avg(carga) from cursos);
``` 
