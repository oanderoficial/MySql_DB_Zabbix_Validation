# Ping do servidor MySQL

```bash
mysqladmin -h <host> -P <porta> -u <user> -p ping
```

# Teste de login e consulta trivial
```bash
mysql -h <host> -P <porta> -u <user> -p -e "SELECT 1;"
```
# Ver versões e identidade (útil pra inventário)
```bash
mysql -u <user> -p -e "SELECT VERSION() AS version, @@hostname AS host, @@port AS port, @@sql_mode AS sql_mode\G"
```
