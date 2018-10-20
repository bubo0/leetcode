# Python3 Points

* ## collections.Counter()
```python3
(import collections)
```
A counter is a container that stores elements as dictionary keys, and their counts are stored as dictionary values.

[https://www.hackerrank.com/challenges/collections-counter/problem]

Sample: 
```python3
>>> from collections import Counter
>>> 
>>> myList = [1,1,2,3,4,5,3,2,3,4,2,1,2,3]
>>> print Counter(myList)
Counter({2: 4, 3: 4, 1: 3, 4: 2, 5: 1})
>>>
>>> print Counter(myList).items()
[(1, 3), (2, 4), (3, 4), (4, 2), (5, 1)]
>>> 
>>> print Counter(myList).keys()
[1, 2, 3, 4, 5]
>>> 
>>> print Counter(myList).values()
[3, 4, 4, 2, 1]
```
### !! Counter[x] == 0 if x does not exist in the Counter

### ?? what is the type of Counter()?
