# Neo4j_Backup_and_Recovery

### FULL AND INCREMENTAL BACKUP
```
neo4j-admin backup --backup-dir=/mnt/neo4j/backups --database=dev2
```
with check consistency
```
neo4j-admin backup --backup-dir=/mnt/neo4j/backups --database=dev2 --check-consistency=false
```
### OFFLINE BACKUP
Be sure to STOP the database first.
```neo4j-admin dump --database=dev2 --to=/mnt/neo4j/dumps/dev2-20220810.dump```
