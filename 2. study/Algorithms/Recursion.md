
#### Factorial
- Time : O(n) goes through all loops so the same as using a while loop in terms of time complexity
- Memory: O(n) saves each function computing during the recursion
``` java
int factorial(int n){
	if n <= 1{
		return 1;
	}
	
	return n * factorial(n-1);
} 
```

``` python
def factorial(n):
	if n<=1;
	return n * factorial(n-1)
```