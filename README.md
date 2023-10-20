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
    Union
        a | b or a.union(b) returns a set containing all unique elements from a and b.

    Intersection
        a & b or a.intersection(b) returns a set containing all elements common to a and b.

    Difference
        a - b or a.difference(b) returns a set containing all elements that are in a but not in b.

    Symmetric Difference
        a ^ b or a.symmetric_difference(b) returns a set containing all elements that are in either a or b, but not both.

    Subset
        a <= b or a.issubset(b) returns True if all elements of a are in b.

    Superset
        a >= b or a.issuperset(b) returns True if all elements of b are in a.

    Disjoint Sets
        a.isdisjoint(b) returns True if a and b have no elements in common.

    Add Element
        a.add(x) adds the element x to the set a.

    Remove Element
        a.remove(x) removes the element x from the set a. If x is not present, it raises a KeyError.

    Discard Element
        a.discard(x) removes the element x from the set a if it is present.

    Pop Element
        a.pop() removes and returns an arbitrary element from the set a. If the set is empty, it raises a KeyError.

    Clear Set
        a.clear() removes all elements from the set a.
