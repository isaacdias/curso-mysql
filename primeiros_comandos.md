# Primeiros comandos no MySQL 

#### Comando para acessar o MySQL localhost:
```
mysql -h localhost -u root -p
```
* -h refere-se ao local
* -u refere-se ao usuário
* -p refere-se a senha que será solicitada logo depois

#### Mostrar os bancos de dados existentes:
```
show databases;
```
#### Criar um banco de dados:
```
create database nome_banco_de_dados;
```
#### Acessar o banco de dados:
```
use nome_banco_de_dados;
```
#### Mostrar as tabelas existentes;

#### Criar uma nova tabela:
```
create table nome_tabela;
```
#### Mostrar a estrutura da tabela:
```
describe nome_tabela; 
```
#### Apagar o banco de dados:
```
drop database nome_banco_de_dados;
```
**default character set utf8**

#### Configurar para linguagem brasileira reconhecendo acentuação:
```
default charset = utf8
```
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
