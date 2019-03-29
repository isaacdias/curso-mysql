* Estrutura da tabela alunos:
```
+----------------+---------------+------+-----+---------+----------------+
| Field          | Type          | Null | Key | Default | Extra          |
+----------------+---------------+------+-----+---------+----------------+
| id             | int(11)       | NO   | PRI | NULL    | auto_increment |
| nome           | varchar(30)   | NO   |     | NULL    |                |
| profissao      | varchar(20)   | YES  |     | NULL    |                |
| nascimento     | date          | YES  |     | NULL    |                |
| sexo           | enum('M','F') | YES  |     | NULL    |                |
| peso           | decimal(5,2)  | YES  |     | NULL    |                |
| altura         | decimal(3,2)  | YES  |     | NULL    |                |
| nacionalidade  | varchar(20)   | YES  |     | Brasil  |                |
| cursopreferido | int(11)       | YES  | MUL | NULL    |                |
+----------------+---------------+------+-----+---------+----------------+
```

* Estrutura da tabela cursos:
```
+-----------+------------------+------+-----+---------+-------+
| Field     | Type             | Null | Key | Default | Extra |
+-----------+------------------+------+-----+---------+-------+
| idcurso   | int(11)          | NO   | PRI | 0       |       |
| nome      | varchar(30)      | NO   | UNI | NULL    |       |
| descricao | text             | YES  |     | NULL    |       |
| carga     | int(10) unsigned | YES  |     | NULL    |       |
| totaulas  | int(10) unsigned | YES  |     | NULL    |       |
| ano       | year(4)          | YES  |     | 2016    |       |
+-----------+------------------+------+-----+---------+-------+
```
* Estrutura da tabela matriculados:
```
+---------+---------+------+-----+---------+----------------+
| Field   | Type    | Null | Key | Default | Extra          |
+---------+---------+------+-----+---------+----------------+
| id      | int(11) | NO   | PRI | NULL    | auto_increment |
| data    | date    | YES  |     | NULL    |                |
| idaluno | int(11) | YES  | MUL | NULL    |                |
| idcurso | int(11) | YES  | MUL | NULL    |                |
+---------+---------+------+-----+---------+----------------+
```
* Registros da tabela alunos:
```
+----+---------------------------+----------------------+------------+------+--------+--------+---------------+----------------+
| id | nome                      | profissao            | nascimento | sexo | peso   | altura | nacionalidade | cursopreferido |
+----+---------------------------+----------------------+------------+------+--------+--------+---------------+----------------+
|  1 | Daniel Morais             | Auxiliar Administrat | 1984-01-02 | M    |  78.50 |   1.83 | Brasil        |              6 |
|  2 | Talita Nascimento         | Farmacêutico         | 1999-12-30 | F    |  55.20 |   1.65 | Portugal      |             15 |
|  3 | Emerson Gabriel           | Programador          | 1920-12-30 | M    |  50.20 |   1.65 | Moçambique    |             10 |
|  4 | Lucas Damasceno           | Auxiliar Administrat | 1930-11-02 | M    |  63.20 |   1.75 | Irlanda       |              7 |
|  5 | Leila Martins             | Farmacêutico         | 1975-04-22 | F    |  99.00 |   2.15 | Brasil        |              2 |
|  6 | Letícia Neves             | Programador          | 1999-12-03 | F    |  87.00 |   2.00 | Brasil        |             17 |
|  7 | Janaína Couto             | Auxiliar Administrat | 1987-11-12 | F    |  75.40 |   1.66 | EUA           |             12 |
|  8 | Carlisson Rosa            | Professor            | 2010-08-01 | M    |  78.22 |   1.98 | Brasil        |             14 |
```
* Registros da tabela cursos:
```
+---------+--------------------+------------------------------------------------------+-------+----------+------+
| idcurso | nome               | descricao                                            | carga | totaulas | ano  |
+---------+--------------------+------------------------------------------------------+-------+----------+------+
|       1 | HTML5              | Curso de HTML5                                       |    40 |       37 | 2014 |
|       2 | Algoritmos         | Lógica de Programação                                |    20 |       15 | 2014 |
|       3 | Photoshop5         | Dicas de Photoshop CC                                |    10 |        8 | 2014 |
|       4 | PHP                | Curso de PHP para iniciantes                         |    40 |       20 | 2015 |
|       5 | Java               | Introdução à Linguagem Java                          |    40 |       29 | 2015 |
|       6 | MySQL              | Bancos de Dados MySQL                                |    30 |       15 | 2016 |
|       7 | Word               | Curso completo de Word                               |    40 |       30 | 2016 |
|       8 | Python             | Curso de Python                                      |    40 |       18 | 2017 |
|       9 | POO                | Curso de Programação Orientada a Objetos             |    60 |       35 | 2016 |
|      10 | Excel              | Curso completo de Excel                              |    40 |       30 | 2017 |
```
* Registros da tabela matriculados:
```
+----+------------+---------+---------+
| id | data       | idaluno | idcurso |
+----+------------+---------+---------+
|  1 | 2014-03-01 |       1 |       2 |
|  2 | 2019-03-01 |      10 |      16 |
|  3 | 2016-09-10 |       3 |      26 |
|  4 | 2013-06-20 |      30 |       9 |
+----+------------+---------+---------+
```

