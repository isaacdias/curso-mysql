# Primeiros comandos no MySQL

**mysql -h localhost -u root -p** 

comando para acessar o MySQL localhost

    -h refere-se ao local

    -u refere-se ao usuário

    -p refere-se a senha que será solicitada logo depois


**show databases;**

- mostra os bancos de dados existentes.

**create database nome_banco_de_dados;**

- cria um banco de dados

**use nome_banco_de_dados;**

- acessa o banco de dados escolhido

**show tables;**

- mostra as tabelas existentes

**create table nome_tabela;**

- cria uma nova tabela

**describe nome_tabela;**

- mostra a estrutura da tabela 

**drop database nome_banco_de_dados;**

- apaga o banco de dados

**default character set utf8**

- configura para linguagem brasileira reconhecendo acentuação

### Criando uma tabela

```
create table pessoas(
    id int not null auto_increment,
    nome varchar (30) not null,
    nascimento date,
    sexo enum ('F', 'M'),
    peso decimal (5,2),
    altura decimal (3,2),
    nacionalidade varchar (20) default 'Brasil',
    primary key (id)
) default charset = uft8;
```
