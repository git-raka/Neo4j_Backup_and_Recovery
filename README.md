# Neo4j_Backup_and_Recovery

### FULL AND INCREMENTAL BACKUP
```
CALL apoc.load.jdbc ("jdbc:postgresql://192.168.1.103/northwind?user=postgres&password=mri123","SELECT * FROM orders WHERE orderdate = '1996-12-23'") yield row 
MERGE (p:orders{id:row.orderid}) 
ON CREATE SET
p.shipper_id=toInteger(row.shipperid),
p.customer_id=toInteger(row.customerid),
p.order_date=datetime(row.orderdate),
p.employee_id=toInteger(row.employeeid)
```
