# Neo4j Backup 

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
```
neo4j-admin dump --database=dev2 --to=/mnt/neo4j/dumps/dev2-20220810.dump
```

# Neo4j Restore
### RESTORE FROM BACKUP
```
neo4j-admin restore --from=/mnt/neo4j/backups/dev2 --database=devx1 --force
```
### RESTORE FROM DUMP
```
neo4j-admin load --from=/mnt/neo4j/dumps/dev2-20220810.dump --database=devx1
```
### RESTORE FROM DUMP IN CLUSTER WITH SEED
```
CALL dbms.cluster.overview();
CREATE DATABASE devx1 OPTIONS {existingData: 'use', existingDataSeedInstance: '<<nodeId-from-cluster>>'};
```


