[source](https://en.wikipedia.org/wiki/Isolation_(database_systems))
## Isolation levels
- Isolation in order of lowest to hig[en.wikipedia.org/wiki/Isolation_(database_systems)](https://en.wikipedia.org/wiki/Isolation_(database_systems))hest transaction isolation level
	- Read uncommited : allows dirty-read
	- Read commited :  no dirty-read but non-repeatable reads possible
	- Repeatable read : phantom reads possible
	- Serializable 
- Read issues from locking
	- dirty-read : reads the uncommitted update of another transaction
	- non-repeatable read :  
	- phantom read : when an entity is added/deleted while transaction of another read was open so the other transaction reads 


## Additional Notes
- MVCC
- why read issues are issues 