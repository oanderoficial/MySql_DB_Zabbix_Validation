# Contador de queries lentas

```bash
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Slow_queries';"
```

# Se o slow log estiver ativo, ver arquivo (ajuste caminho)

```bash
mysql -u <user> -p -e "SHOW VARIABLES LIKE 'slow_query_log%';"
mysql -u <user> -p -e "SHOW VARIABLES LIKE 'long_query_time';"
# (no SO) grep/cut no slow.log
sudo grep -i "Query_time" /var/lib/mysql/*slow*.log | tail -n 50
```
