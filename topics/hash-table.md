# Hash Table

## 1 Signs/hints
* Need to return the number of possible combinations in a list

## 2 Difficulties/easily overlooked parts
* set up what the key and value are for a hashmap 

## 3 General techniques
* HashSet: [Set](https://docs.python.org/3/tutorial/datastructures.html#sets)
```python3
>>> basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
>>> print(basket)                      # show that duplicates have been removed
{'orange', 'banana', 'pear', 'apple'}
>>> 'orange' in basket                 # fast membership testing
True
>>> 'crabgrass' in basket
False

>>> basket.add('melon')                # add elemnets (does not return value)
>>> basket.remove('apple')             # remove elements (does not return value)
>>> # Demonstrate set operations on unique letters from two words
...
>>> a = set('abracadabra')
>>> b = set('alacazam')
>>> a                                  # unique letters in a
{'a', 'r', 'b', 'c', 'd'}
>>> a - b                              # letters in a but not in b
{'r', 'd', 'b'}
>>> a | b                              # letters in a or b or both
{'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}
>>> a & b                              # letters in both a and b
{'a', 'c'}
>>> a ^ b                              # letters in a or b but not both
{'r', 'd', 'b', 'm', 'z', 'l'}
```
* HashMap: [dict](https://docs.python.org/3/tutorial/datastructures.html#dictionaries), collection.Counter()
```python3
>>> tel = {'jack': 4098, 'sape': 4139}
>>> tel['guido'] = 4127
>>> tel
{'jack': 4098, 'sape': 4139, 'guido': 4127}
>>> tel['jack']
4098
>>> del tel['sape']
>>> tel['irv'] = 4127
>>> tel
{'jack': 4098, 'guido': 4127, 'irv': 4127}
>>> list(tel)
['jack', 'guido', 'irv']
>>> sorted(tel)
['guido', 'irv', 'jack']
>>> 'guido' in tel
True
>>> 'jack' not in tel
False
```

## 4 Problems and solutions
Problems | Solutions | Difficulty
-------- | --------- | ----------
[001. Two Sum](https://leetcode.com/problems/two-sum/description/) | [Python3](../algorithms/001.twoSum.md) | E
[560. Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/description/) | [Python3](../algorithms/560.subarraySumEqualsK.md) | M
[525. Contiguous Array](https://leetcode.com/problems/contiguous-array/description/) | [Python3](525.ContiguousArray.md) | M
[000.]() | [Python3]() | .
