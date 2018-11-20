# Python3 Tricks

* ## collections.Counter()
```python3
(import collections)
```
A counter is a container that stores elements as **dictionary** keys, and their counts are stored as dictionary values.
[ref](https://www.hackerrank.com/challenges/collections-counter/problem)

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

* ## !! for i in range(len(nums)):
Notice that "for i in nums:" means traversal of elements, not indices

* ## Queue
[ref](https://blog.csdn.net/GeekLeee/article/details/77883252)
```python3
from queue import Queue             # 1

q = Queue()                         # 2

for i in range(3):
    q.put(i)                        # 3

while not q.empty():                # 4
    print(q.get())                  # 5
# by default, a queue is FIFO
# output:
# 0
# 1
# 2

```
LifoQueue:
```python3
from queue import LifoQueue

q = LifoQueue()

for i in range(3):
    q.put(i)

while not q.empty():
    print(q.get())
# output:
# 2
# 1
# 0
```
PriorityQueue  
(The version in the Queue module is implemented using the heapq module, so they have equal efficiency for the underlying heap operations.)
```python3
from queue import PriorityQueue


class Job(object):
    def __init__(self, priority, description):
        self.priority = priority
        self.description = description
        print('New job:', description)
        return

    def __lt__(self, other):
        return self.priority < other.priority

q = PriorityQueue()

q.put(Job(5, 'Mid-level job'))
q.put(Job(10, 'Low-level job'))
q.put(Job(1, 'Important job'))

while not q.empty():
    next_job = q.get()
    print('Processing job', next_job.description)
```
* ## set.discard(x)

This operation also removes element  from the set. 
If element  does not exist, it **does not** raise a KeyError.
The .discard(x) operation returns None.

* ## Using Lists as Stacks
[ref](https://docs.python.org/3/tutorial/datastructures.html#using-lists-as-stacks)
```python3
>>> stack = [3, 4, 5]
>>> stack.append(6)
>>> stack.append(7)
>>> stack
[3, 4, 5, 6, 7]
>>> stack.pop()
7
>>> stack
[3, 4, 5, 6]
>>> stack.pop()
6
>>> stack.pop()
5
>>> stack
[3, 4]
```
* ## remove punctuations from a string
```python3
translator = str.maketrans('', '', string.punctuation) # "str" is a type in Python3. Don't change it
res = original_string.translate(translator)
```
* ## remove spaces from a string
```python3
s.replace(' ','')
```

* ## capital letters to lower-case letters:
```python3
s.lower()
s.upper()
s.islower() # return whether letters in s are all lower-case
s.isupper() # return whether letters in s are all upper-case
```
