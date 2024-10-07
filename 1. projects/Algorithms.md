## History
- 

### Hashing
- key-value pair using hashing function
- has no duplicates and no order -> makes indorder traversal inefficient
- useful for finding unique, count, frequency
- Hash Sets :
	- ``hashset = set() hashset.add(n) hashset.remove(n)``
- Hash Maps : Similar to  hash sets but keys point to another seperate value
	- insert, remove, search O(1)  worst case O(n)
	- inorder O(nlogn)
	- space O(n) n is porpotional to unique keys
	- if key doesn't exist ``hashmap[key]`` throws an error. use ``hashmap.get(key, default_value)``
	- ``hashmap = {} hashmap[key] = n``
- TreeMap:
	- insert, remove, serach O(logn)
	- inorder O(n)