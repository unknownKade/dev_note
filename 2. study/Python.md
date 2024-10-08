Python specific syntax and features to remember
### List Comprehension
```python
[n * 2 for n in range(1, 10 + 1)]
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