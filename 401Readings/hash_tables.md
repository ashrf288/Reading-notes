## Hashtables

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value



![](https://he-s3.s3.amazonaws.com/media/uploads/dda3e36.jpg)


## hash



+ Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

Hashtables are a data structure that utilize `key` `value` pairs. This means every `Node` or `Bucket` has both a key, and a value.



+ Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.


example :

```
["Greenwood:98103", "Downtown:98101", "Alki Beach:98116", "Bainbridge Island:98110", ...]
```

+ Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.


## Structure

 1- Hashing   (hash code turns a key into an integer)

heir output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.


## Collisions

A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.


If two keys ever ultimately resolved to the same index, then two calls to .Add(key, val) with different keys would overwrite each other.


Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.



If we didn’t store the key, the bucket would look like this. Accessing .get("Pioneer Square") or .get("Alki Beach") would hash the keys and still lead to bucket 92, but it would be impossible to tell which of the zip code values there to return.



## Hash maps do this to store values:

+ accept a key
+ calculate the hash of the key
+ use modulus to convert the hash into an array index
+ store the key with the value by appending both to the end of a + linked list

## Hash maps do this to read value:

+ accept a key
+ calculate the hash of the key
+ use modulus to convert the hash into an array index
+ use the array index to access the short LinkedList representing a bucket
+ search through the bucket looking for a node with a key/value pair that matches the key you were given


## Bucket Sizes

It’s possible to compute the “load factor” of a hash table. The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.


## Internal Methods


+ **Add()**
When adding a new key/value pair to a hashtable:


send the key to the GetHash method.
Once you determine the index of where it should be placed, go to that index
Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
If something does exist, add the new key/value pair to the data structure within that bucket.

+ **Find()**
The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.


+ **Contains()**
The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.


+ **GetHash()**
The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

[more details ](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
