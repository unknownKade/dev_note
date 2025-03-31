
#### Factorial
n! = n *  (n-1)!
Time : O(n) Memory: O(n)
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