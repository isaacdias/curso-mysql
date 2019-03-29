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
#### Filtrarppor linha os registros que serão exibidos:
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
