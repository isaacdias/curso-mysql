# Manipulando registros

#### Alterar o registro de uma tabela:
* utilizar a chave primária para identificar onde será alterado
```
update nome_tabela
set nome_coluna = ‘novo_registro’
where coluna_chave_primaria = ‘chave_primaria’;
```
* Alterando mais de uma registro ao mesmo tempo
* limit serve para limitar a quantidade de linhas que serão alteradas
```
update nome_tabela
set nome_coluna = ‘novo_registro’, set nome_coluna = 'novo_registro
where coluna_chave_primaria = ‘chave_primaria’
limit 1;
```
#### Apagar uma linha da tabela:
```
delete from nome_tabela
where primary_hey = 'x';
```
#### Apagar todos os registros de uma tabela:
```
truncate nome_tabela;
```

