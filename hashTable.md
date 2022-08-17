# Hash Table

Terminology:

**Hash** - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

**Buckets** - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

**Collisions** - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

# How to implement Hash Tables in JavaScript
Firstly, create a class for the hash table.

Define a hash function.

Define a method for adding key-value pairs for the hash tables.

![](./image/hash%20Table.png)