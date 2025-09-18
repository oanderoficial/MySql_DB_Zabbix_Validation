# Top 15 maiores tabelas do schema atual

```bash
mysql -u <user> -p zabbix -e "
SELECT table_name,
       engine,
       table_rows,
       ROUND((data_length+index_length)/1024/1024,2) AS size_mb
FROM information_schema.tables
WHERE table_schema = DATABASE()
ORDER BY size_mb DESC
LIMIT 15;"

```

# Somatório total do schema

```bash
mysql -u <user> -p zabbix -e "
SELECT ROUND(SUM(data_length+index_length)/1024/1024,2) AS total_mb
FROM information_schema.tables
WHERE table_schema = DATABASE();"
```
