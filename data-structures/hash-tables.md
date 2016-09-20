## hash tables

#### how do hash tables work?
  * maps values to keys
  * allows constant time lookup for key/value pairs

#### use cases:
  * lookups
  * preventing duplicates
  * caching
    * websites map URLs to their corresponding data

#### hash functions:
  * map strings to numbers
  * requirements:
    * consistent: will give the same output for a certain input every time
    * should map ever string to a different number, for the most part
    * only returns valid indexes

#### collisions:
  * occur when multiple keys are assigned to the same index
  * solution: start linked list at that index
  * how do you avoid collisions?
    * good hash function
    * low ratio of total items to total slots (load factor)

#### resizing:
  * rule of thumb: double capacity when load factor is greater than 0.7
  * create new hash table with double the slots of the old one
  * redistribute old hash table's items to new hash table using hash function

#### time complexities:
  * __lookup:__ O(1) -> constant time
  * __insertion:__ O(1) -> constant time
  * __deletion:__ O(1) -> constant time

#### implementation:
  * coming soon
