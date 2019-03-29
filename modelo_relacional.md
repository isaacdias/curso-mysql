## Modelo relacional

#### um-para-um
* pegue a chave primária da outra entidade e transfira na entidade dominante

#### um-para-muitos
* pegue a chave primária do lado um e transfira para muitos

#### muitos-para-muitos
* é criada uma nova entidade que faz a ligação entre as entidades, desmembrando a relação muitos-para-muitos.

**chave estrangeira é alguma chave primária de algum lugar que veio para outro lugar**

#### Fazendo relações entre tabelas um-para-muitos
```
alter table nome_tabela
add nome_coluna int;
```
```
alter table
add foreign key (nome_coluna)
references nome_tabela(nome_chave_primaria);
```
```
update alunos
-> set cursopreferido = '6'
-> where id = '1';
```
#### Junções SQL
* Aqui conseguimos exibir registros das duas tabelas ao mesmo tempo fazendo uma junção.

```
select alunos.nome, alunos.cursopreferido, cursos.nome, cursos.ano
from alunos join cursos
on cursos.idcursos = alunos.cursopreferido
order by alunos.nome;
```
* Exibe todas as informações dando preferencia a tabela da esquerda do join
```
select a.nome, c.nome, c.ano
from alunos as a left outer join cursos as c
on a.cursopreferido = c.idcurso;
```
* Exibe todos as relações dando prioridade a tabela da direita do join
```
select a.nome, c.nome, c.ano
from alunos as a right outer join cursos as c
on a.cursopreferido = c.idcurso;
```
#### Muitos-para-muitos
```
create table matriculados(
id int not null auto_increment,
data date,
idaluno int,
idcurso int,
primary key(id),
foreign key (idaluno) references alunos(id),
foreign key (idcurso) references cursos(idcurso)
) default charset = utf8;
```

```
insert into matriculados values
(default, '2014-03-01', '1', '2');
```

```
select a.nome, c.nome from aluno a 
join matriculados m 
on a.id = m.idaluno
join cursos c on c.idcurso = m.idcurso 
order by g.nome;
```
