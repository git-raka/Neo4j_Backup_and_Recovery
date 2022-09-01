# Neo4j_Backup_and_Recovery

### FULL AND INCREMENTAL BACKUP
```
neo4j-admin backup --backup-dir=/mnt/neo4j/backups --database=dev2
```
with check consistency
```
neo4j-admin backup --backup-dir=/mnt/neo4j/backups --database=dev2 --check-consistency=false
```
