# Janela de dados presente nas tabelas de histórico/trends

```bash
mysql -u <user> -p zabbix -e "SELECT 'history' AS tbl, FROM_UNIXTIME(MIN(clock)) min_t, FROM_UNIXTIME(MAX(clock)) max_t FROM history;"
mysql -u <user> -p zabbix -e "SELECT 'history_uint', FROM_UNIXTIME(MIN(clock)), FROM_UNIXTIME(MAX(clock)) FROM history_uint;"
mysql -u <user> -p zabbix -e "SELECT 'history_text', FROM_UNIXTIME(MIN(clock)), FROM_UNIXTIME(MAX(clock)) FROM history_text;"
mysql -u <user> -p zabbix -e "SELECT 'history_log', FROM_UNIXTIME(MIN(clock)), FROM_UNIXTIME(MAX(clock)) FROM history_log;"
mysql -u <user> -p zabbix -e "SELECT 'trends', FROM_UNIXTIME(MIN(clock)), FROM_UNIXTIME(MAX(clock)) FROM trends;"
mysql -u <user> -p zabbix -e "SELECT 'trends_uint', FROM_UNIXTIME(MIN(clock)), FROM_UNIXTIME(MAX(clock)) FROM trends_uint;"
````

# Itens com maior retenção configurada (history/trends em dias)

```bash
mysql -u <user> -p zabbix -e "
SELECT i.itemid, h.host, i.name, i.history, i.trends
FROM items i
JOIN hosts h USING(hostid)
ORDER BY i.history DESC, i.trends DESC
LIMIT 20;"
```
