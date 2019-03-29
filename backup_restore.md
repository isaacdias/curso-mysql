## Backup e Restore de uma banco de dados MySQL

#### Criar backup:
```
mysqldump -u root -p nome_banco_de_dados >
/homw/usuario/nome_banco_de_dados.sql
```
#### Restaurar banco de dados:
* Crie um banco de dados novo no servidor.
```
mysql -u root -p nome_banco_de_dados_novo <
/home/usuario/backup_banco_de_dados.sql
```
