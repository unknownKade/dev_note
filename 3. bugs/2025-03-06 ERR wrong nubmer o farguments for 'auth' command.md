### Occurance
Occured while trying to connect Docker Redis DB on intellij
Returned following error
```
DMS: Redis(no ver.)
Case sensitvity: plain=mixed, delimited=exact

ERR wrong number of argmuents for 'auth' command.
```
### Issue
Windows was running a redis server as well.

### Solution
Stop Redis server on Windows (from local service) or stop Docker Redis