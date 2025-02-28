## Git Flow
- Vincent Driessen이 2010년에 제시한 브랜치 전략으로 용도 별로 브랜치를 각종 단계를 나아가며 머지한다.
- 정교하고 안정적이지만 복잡하다
- 브랜치 종류
	- master(main)
	- hotfix : 급한 수정
	- release : 배포 버전별 브랜치
	- develop : 개발 중인 브랜치
	- feature : 개발하는 기능 별 브랜치

````bash
#브랜치 바꾸기
checkout
switch
restore
````

## Trunk Based Development
 - 트렁크 기반 개발은 'trunk'로 분류한 한 브랜치에 기능 별 브랜치를 만들어 커밋하고 trunk에서 릴리즈 버전 브랜치를 따로 빼는 전략
 - main에 feat을 바로 merge하고 release 브래치를 따로 뗀다.
 - 작은 기능 개발에 대해서는 복잡성이 줄어들어 편리하지만 큰 기능은 머지하기 어려워집니다.
 - 빠르고 간단하지만 안정성이 떨어진다