# MySql_DB_Zabbix_Validation
Validation in the Zabbix database 


```sql
-- Verificar conexões no banco

SHOW PROCESSLIST;

-- Verifica limites de conexão
SHOW VARIABLES LIKE 'max_connections';
SHOW GLOBAL STATUS LIKE 'Max_used_connections';

-- Verifica tempo de espera de conexões inativas
SHOW VARIABLES LIKE 'wait_timeout';
SHOW VARIABLES LIKE 'interactive_timeout';

-- Verifica tamanho máximo de pacote permitido
SHOW VARIABLES LIKE 'max_allowed_packet';

-- Verifica tamanho do buffer de InnoDB
SHOW VARIABLES LIKE 'innodb_buffer_pool_size';
SHOW VARIABLES LIKE 'innodb_log_file_size';

-- Verifica quantidade atual de conexões
SHOW STATUS LIKE 'Threads_connected';

-- Verifica número de conexões abortadas
SHOW STATUS LIKE 'Aborted_connects';

-- Verifica conexões atualmente em uso
SHOW STATUS LIKE 'Threads_running';

-- Verifica queries lentas
SHOW VARIABLES LIKE 'slow_query_log';
SHOW VARIABLES LIKE 'long_query_time';

-- Verifica uso atual do buffer de InnoDB
SHOW ENGINE INNODB STATUS\G

-- Verifica uso de tabelas temporárias
SHOW GLOBAL STATUS LIKE 'Created_tmp_disk_tables';
SHOW GLOBAL STATUS LIKE 'Created_tmp_tables';

-- Verifica tempo médio de bloqueio
SHOW GLOBAL STATUS LIKE 'Innodb_row_lock_time_avg';

-- Verifica tabelas abertas
SHOW STATUS LIKE 'Open_tables';
SHOW STATUS LIKE 'Opened_tables';

-- Verifica o total de conexões feitas
SHOW STATUS LIKE 'Connections';
```
