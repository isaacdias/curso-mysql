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
#### Combinafr operadores lógicos com operadores relacionais:
* nesse exemplo será mostrado os registros com carga maior que 30 e total de aulas menou ou igual a 20.
```
select * from cursos
where carga > 30 and totaulas <= 20
order by totaulas;
```

