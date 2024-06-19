- 멀티스레드 프로그램에서 스레드가 동기화 되어있지 않으면 data의 안정성과 신뢰성을 보장 할 수 없다.
- 자바에서는 synchronized 키워드로 thread-safe 가능
- 데이터를 한 스레드만 쓸 수 있도록 다른 스레드는 데이터에 접근 할 수 없게 막는다
- 변수와 함수에 사용할 수 있다.
- 자바 내부적으로 block/unblock 처리를 하기 때문에 처리가 많아지면 성능저하를 일으킬 수 있다


## 메소드에 사용

```java
public class ThreadSynchronizedTest{
	public static void main(String[] args){
		Task task = new Taks();
		Thread t1 = new Thread(task);
		Thread t2 = new Thread(task);
		t1.setName("thread 1");
		t2.setName("thread 2");
		t1.start();
		t2.start();
	}
}

class Acount{
	int balance = 1000;

	pbulic void withDraw(int money){
		if(balance >= money){
			try{
				//출금
				Thread thread = Thread.currentThread();
				Thread.sleep(1000);
				balance -=money;
			}catch(Exception e){}
		}
	}
}

class Task implements Runnable{
	Account acc = new Account();

	public void run(){
		while(acc.balance > 0){
			int money = (int) (Math.random() * 3 + 1) * 100;
			acc.withDraw(money);
		}
	}
}
```

