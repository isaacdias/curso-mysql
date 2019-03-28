## Manipulando uma tabela

**DML – data manipulation language**

#### Inserindo dados na tabela:
```
insert into nome_tabela values
(defalut, ‘isaac’, ‘1990-05-27’, ‘M’, ‘68,8’, ‘1,75’, ‘Brasil’);
```
#### Mostrando os registro e uma tabela:
```
select * from nome_tabela
```
## Alterando estrutura de uma tabela (alter table)

#### Adicionar uma nova coluna a tabela
```
alter table nome_tabela
add column nome_da_coluna varchar (10);
``` 
```
alter table nome_tabela
add column nome_da_coluna varchar (10) after nome_coluna_existente;
```
```
alter table nome_tabela
add column nome_da_coluna varchar (10) first;
```
#### Remover uma coluna
```
alter table nome_tabela
drop column nome_da_coluna;
```


