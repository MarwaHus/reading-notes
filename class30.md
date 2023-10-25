# Hash Tables

### What is Hash Tables:<br>
a hash table (or hash map) is a data structure that is used to store key-value pairs. It uses a function (called a hash function) to compute an index into an array of buckets or slots, from which the desired value can be found.
### Why use a hash table?<br>
Hash tables are useful because they allow for very fast lookup, insertion, and deletion of data. The average time complexity for these operations is O(1), which means that they can be performed very quickly even for large amounts of data.
### How does a hash table work?<br>
A hash table consists of an array of buckets or slots, where each slot contains a key-value pair or is empty. When a new value is inserted into the hash table, its key is first hashed to compute an index in the array. If the slot is empty, the key-value pair is stored in that slot. If the slot is already occupied, a collision occurs.
### Hashtable class declaration
```
public class Hashtable<K,V> extends Dictionary<K,V> implements Map<K,V>, Cloneable, Serializable
```
### Hashtable class Parameters
K: It is the type of keys maintained by this map.
V: It is the type of mapped values.

### Hashtable Methods
The methods in Hashtable class are very similar to HashMap. Take a look.

* void clear() : It is used to remove all pairs in the hashtable.
* boolean contains(Object value) : It returns true if specified value exist within the hash table for any pair, else return false. Note that this method is identical in functionality to containsValue() function.
* boolean containsValue(Object value) : It returns true if specified value exist within the hash table for any pair, else return false.
* boolean containsKey(Object key) : It returns true if specified key exist within the hash table for any pair, else return false.
* boolean isEmpty() : It returns true if the hashtable is empty; returns false if it contains at least one key.
* void rehash() : It is used to increase the size of the hash table and rehashes all of its keys.
* Object get(Object key) : It returns the value to which the specified key is mapped. Returns null if no such key is found.
* Object put(Object key, Object value) : It maps the specified key to the specified value in this hashtable. Neither the key nor the value can be null.
* Object remove(Object key) : It removes the key (and its corresponding value) from hashtable.
int size() : It returns the number of entries in the hash table.
### Hashtable Performance
Performance wise HashMap performs in O(log(n)) in comparion to O(n) in Hashtable for most common operations such as get(), put(), contains() etc.
