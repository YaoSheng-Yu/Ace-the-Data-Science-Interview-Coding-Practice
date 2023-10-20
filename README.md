# Ace-the-Data-Science-Interview-Coding-Practice
Record for practice problem

#1
Given two arrays, write a function to get the intersection of the two. For example, if A = [1,2,3,4,5], and B = [0,1,3,7] then you should return [1,3]

---------------------------------------
**Solution1** array O(n*m)
```python
def array_intersection(a, b):
    if len(a) < len(b):
        return [x for x in a if x in b]
    else:
        return [x for x in b if x in a]

```

**Solution2** set O(n+m)
```python
def array_intersection(a, b):
  set_a = set(a)
  set_b = set(b)
  intersect = set_a & set_b
  return list(intersect)

```

Common operation for set:
    Union: set_a | set_b or set_a.union(set_b) will return a set containing all unique elements from set_a and set_b.

    Intersection: set_a & set_b or set_a.intersection(set_b) will return a set containing all elements that are common to set_a and set_b.

    Difference: set_a - set_b or set_a.difference(set_b) will return a set containing all elements that are in set_a but not in set_b.

    Symmetric Difference: set_a ^ set_b or set_a.symmetric_difference(set_b) will return a set containing all elements that are in either set_a or set_b, but not both.

    Subset: set_a <= set_b or set_a.issubset(set_b) will return True if all elements of set_a are in set_b.

    Superset: set_a >= set_b or set_a.issuperset(set_b) will return True if all elements of set_b are in set_a.

    Disjoint: set_a.isdisjoint(set_b) will return True if set_a and set_b have no elements in common.

    Add: set_a.add(x) will add the element x to set_a.

    Remove: set_a.remove(x) will remove the element x from set_a. If x is not in set_a, it will raise a KeyError.

    Discard: set_a.discard(x) will remove the element x from set_a if it is present. If x is not in set_a, it does nothing.

    Pop: set_a.pop() will remove and return an arbitrary element from set_a. If set_a is empty, it raises a KeyError.

    Clear: set_a.clear() will remove all elements from set_a.
