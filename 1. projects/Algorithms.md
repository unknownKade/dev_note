## History
- 유클리드 호제법(최대공약수)
- 가우스 소거법(방정식)
- 사다리꼴의 법칙(정적분)
- dijkstra's algorithm (shortest route)
- Sieve of Eratosthenes (prime numbers)

## Sort
- straight selection sort 단순 선택 정렬
- straight insertion sort 단순 삽입 정렬
- bubble sort 단순 교환 정렬
- shell sort
- merge sort 병합 정렬
- quick sort 퀵 정렬
- heap sort

## Search
- linear search 선형 검색
- binary search 이진 검색
	- search array
	- search range
-  String Pattern Matching
	- 단순 문자열 일치
	- KMP algorithm
	- BN algorithm


## Hashing
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