# Uptime e conexões ativas

```bash
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Uptime';"
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Threads_connected';"
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Threads_running';"
```

# QPS aproximado (Questions por segundo; rode duas vezes e compare)
```bash
mysql -u <user> -p -e "SHOW GLOBAL STATUS LIKE 'Questions';"
```
