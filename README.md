# Design HashSet
## https://leetcode.com/problems/design-hashset

Design a HashSet without using any built-in hash table libraries.

Implement MyHashSet class:
```
void add(key) Inserts the value key into the HashSet.

bool contains(key) Returns whether the value key exists in the HashSet or not.

void remove(key) Removes the value key in the HashSet. If key does not exist in the HashSet, do nothing.
```

## Implementation : Using ArrayList
```java
class MyHashSet {
    List<Integer> list;
    public MyHashSet() {
        list = new ArrayList<Integer>();
    }
    
    public void add(int key) {
        for(int num : list) {
            if(num == key)
                return;
        }
        list.add(key);
    }
    
    public void remove(int key) {
        list.remove(new Integer(key));
    }
    
    public boolean contains(int key) {
        return list.contains(key);
    }
}
```
