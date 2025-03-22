
# 📌 LeetCode Problem:[290. Word Pattern](https://leetcode.com/problems/word-pattern/description/)

# **Problem statement:-Design a HashSet without using any built-in hash table libraries.

**Implement MyHashSet class:

****void add(key) Inserts the value key into the HashSet.**
bool contains(key) Returns whether the value key exists in the HashSet or not.**
**void remove(key) Removes the value key in the HashSet. If key does not exist in the HashSet, do nothing.**


### Solution:-

``` java



class MyHashSet {
HashSet<Integer>MyHashSet;

    public MyHashSet() {
        MyHashSet=new HashSet<>();
    }
    
    public void add(int key) {
      MyHashSet.add(key);
        
    }
    
    public void remove(int key) {
        if(MyHashSet.contains(key)){
            MyHashSet.remove(key);
        }
    }
    
    public boolean contains(int key) {
        if(MyHashSet.contains(key)){
            return true;
        }
    return false;
    }
}

/**
 * Your MyHashSet object will be instantiated and called as such:
 * MyHashSet obj = new MyHashSet();
 * obj.add(key);
 * obj.remove(key);
 * boolean param_3 = obj.contains(key);
 */
