# ANALYZE (atualiza estatísticas de índices) - leve

```bash
mysql -u <user> -p zabbix -e "
ANALYZE TABLE history, history_uint, history_text, history_log, trends, trends_uint, events, acknowledges, problem, problem_tag;"
```

# CHECK TABLE (verificação lógica/índices) - use com cautela em horário de baixo uso

```bash
mysql -u <user> -p zabbix -e "
CHECK TABLE history, history_uint, history_text, history_log, trends, trends_uint, events, acknowledges, problem, problem_tag;"
```
