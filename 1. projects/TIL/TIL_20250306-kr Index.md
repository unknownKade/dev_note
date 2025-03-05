읽기 퍼포먼스를 향상시키기 위한 추가적인 자료구조. 인덱스가 커지면 인덱스가 차지하는 용량이 많아지는 것과 쓰기/수정할 때 계속 인덱스가 업데이트 되어야하기 때문에 쓰기/수정 성능이 떨어지는것이 단점이다.  


#### 인덱스 구현방법들 
- Hash Index
	- in memory hash map으로 인덱스를 구현하면 RAM에 키와 디스크 상 주소를 저장할 수 있다. Dictionary Lookup으로 읽는다
	- update가 많을수록 불필요한 데이터가 많아져서 파일을 최대용량만큼 잘라 immutable로 저장하는 Segement File과 Segement File을 정리해서 실제로 데이터로 췽합하는 Compaction로 보완. immutable segment file로 저장하고 정리하는 프로세스를 통해 유저가 수정하지 못하게 하므로써 성능이 향상된다 
	- Bitcask key/value store에서 사용
- B Tree
- B+ Tree
- LSM Tree
	- Sorted String Table 

#### 참고
[LSM Tree](https://www.youtube.com/watch?v=i_vmkaR1x-I)

[LSM Tree](https://www.youtube.com/watch?v=I6jB0nM9SKU)