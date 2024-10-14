Python specific syntax and features to remember


### Synatxes I get wrong often
```python
string.lower()
len(arr)
```
### Filters and Searching
```python
re.findAll()
list.find(word)

```

### Data Structure methods
```python
arr.append() #push
arr.pop() #actual real pop
arr[-1] #peek last element
arr[i:j] #index i to j
arr[i:] # from index i including i
arr[:i] # up to i from back 
arr
```
### List Comprehension
```python
[n * 2 for n in range(1, 10 + 1) if n %2 == 1]
```

### Generator
```python
yield
```

### Enumerate
```python
for index, value in enumerate(a) :
	print(a[i] == value)
```
### Operators
``` python
5//3 #1
divmod(5,3) # (1,2)
```
### Print
```python
print('aa', 'bb', sep = ',') # aa,bb
print('aa', end = 'b') #aab
print(' '.join(['A', 'B'])) # A B
print('{0}:{1}'.format(idx + 1, "Apple"))
```

### Locals
```python
import pprint
pprint.pprint(locals())
```


### Immutable Object
```python
def foo(a, b=None)
def foo(a, b: Optional[Sequence] = None)
```