# Hash Tables

* Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

* Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

* Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

* Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

* A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

* A hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

* A hash table is traditionally created from an array. After the array is created, you can do some sort of logic to turn a *key* into a numerical number value.
    * Add or multiply all the ASCII values together.
    * Multiply it by a prime number such as 599.
    * Use modulo to get the remainder of the result, when divided by the total size of the array.
    * Insert into the array at that index.

* The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

* Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a `LinkedList` in each one!

### Internal Methods

* `Add()` : When adding a new key/value pair to a hashtable:
    * send the key to the GetHash method.
    * Once you determine the index of where it should be placed, go to that index
    * Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    * If something does exist, add the new key/value pair to the data structure within that bucket.

* `Find()` : takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

* `Contains()` : accepts a key, and return a bool on if that key exists inside the hashtable.

* `GetHash()` : accepts a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.