# Lista de sessões/queries

```bash
mysql -u <user> -p -e "SHOW FULL PROCESSLIST;"
```

# Top 10 digests por tempo total (se performance_schema estiver ativo)

```bash
mysql -u <user> -p -e "
SELECT DIGEST_TEXT, COUNT_STAR calls, ROUND(SUM_TIMER_WAIT/1e12,1) total_s
FROM performance_schema.events_statements_summary_by_digest
ORDER BY SUM_TIMER_WAIT DESC LIMIT 10;"
```
