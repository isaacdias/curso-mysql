## Manipulando uma tabela

**DML – data manipulation language**

#### Inserir dados na tabela:
```
insert into nome_tabela values
(defalut, ‘isaac’, ‘1990-05-27’, ‘M’, ‘68,8’, ‘1,75’, ‘Brasil’);
```
#### Mostrar os registros de uma tabela:
```
select * from nome_tabela
```
## Alterando estrutura de uma tabela (alter table)

#### Adicionar uma nova coluna a tabela:
* adiciona a coluna na utima posição
```
alter table nome_tabela
add column nome_da_coluna varchar (10);
``` 
* adiciona a coluna após outra coluna escolhida
```
alter table nome_tabela
add column nome_da_coluna varchar (10) after nome_coluna_existente;
```
* adiciona a coluna na primeira posição
```
alter table nome_tabela
add column nome_da_coluna varchar (10) first;
```
#### Remover uma coluna:
```
alter table nome_tabela
drop column nome_da_coluna;
```
#### Alterar a definição da coluna:
```
alter table nome_tabela
modify column nome_da_coluna varchar (20); 
```
#### Alterar o nome da coluna:
```
alter table nome_tabela
change column nome_atual_da_coluna nome_novo varchar (20); 
```
#### Alterar o nome da tabela:
```
alter table nome_tabela
rename to nome_novo;
```
#### Tornar uma coluna como chave primária:
```
alter table nome_tabela
add primary key (nome_coluna);
```

#### Exemplo de uma tabela:
```
create table if not exists cursos (
nome varchar(30) not null unique,
descricao text,
carga int unsigned,
totaulas int unsigned,
ano year default '2016'
) default charset=utf8;
```
* unique é diferente de primary key

