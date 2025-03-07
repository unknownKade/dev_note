읽기 퍼포먼스를 향상시키기 위한 추가적인 자료구조. 인덱스가 커지면 인덱스가 차지하는 용량이 많아지는 것과 쓰기/수정할 때 계속 인덱스가 업데이트 되어야하기 때문에 쓰기/수정 성능이 떨어지는것이 단점이다.  

#### 인덱스 구현방법들 
[[TIL_250306-kr HashIndex]]
- B Tree
	- 
- B+ Tree
	- 
- LSM Tree
	- Sorted String Table 
	- Incoming writing is stored in inmemory storage **memtable** (appended to log file to prevent data loss)

#### 참고
[LSM Tree-kr](https://www.youtube.com/watch?v=i_vmkaR1x-I)
[B-Tree](https://www.youtube.com/watch?v=K1a2Bk8NrYQ)
[B+Tree-kr](https://www.youtube.com/watch?v=yLe7_3cGSeU)
[LSM Tree](https://www.youtube.com/watch?v=I6jB0nM9SKU)