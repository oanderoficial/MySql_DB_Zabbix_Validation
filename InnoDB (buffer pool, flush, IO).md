# Tamanho do buffer pool e páginas

```bash
mysql -u <user> -p -e "SHOW VARIABLES LIKE 'innodb_buffer_pool_size';"
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Innodb_buffer_pool%';"
```
# Indicadores comuns

```bash
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Innodb_rows_%';"
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Innodb_os_log_written';"
```

# Relatório detalhado (cuidado: pesado de ler, mas útil)

```bash
mysql -u <user> -p -e "SHOW ENGINE INNODB STATUS\G"
```
