# Hash Tables

### Terminology
- **Hash**: The result of taking an incoming string and converting it into a value that can be used for security purposes or other purposes. For a hashtable, it is used to determine the index of the array.
- **Buckets**: In a hashtable, each index of the array and the contents is a bucket. An index can contain multiple key/value pairs if a collision occurs. 
- **Collisions**: A collision occurs when more than one key hashes to the same index in an array.
- The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.
- Collisions are solved by changing the initial state of buckets. Instead of null, we can initialize a `LinkedList`.
- **Use**: Hold unique values, dictionary, library
- **Hashtable**: Data structure that utilizes key/value pairs. This means every `Node` or `Bucket` has both a key and a value. 
- A hashtable allows the ability to store the key into this data structure and quickly retrieve it. 
- This is done with a **hash**.
- A **hash** is the ability to encode the key that will eventually map to a specific location in the data structure to retrieve the value. 
- **Hash code** turns a key into an integer. Deterministic: their output is determined only by their input - the same key should always produce the same hash code. 
- **Creating a hash**: 
    - A hashtable is traditionally created from an array 
    - Create array of appropriate size for index placement
    - Add or multiply all ASCII values together
    - Multiply by a prime number such as 599
    - Use modulo to get remainder of result, when divided by total size of array
    - Insert into array at that index
 - **Hash maps do this to store values:**
    - Accept a key
    - Calculate the hash of the key
    - Use modulus to convert has into array index
    - Store key with value by appending both to end of linked list 
 - **Hash maps do this to read values:**
    - Accept a key
    - Calculate the hash of the key
    - Use modulus to convert the hash into an array index
    - Use the array index to access the short LinkedList representing a bucket
    - Search through the bucket looking for a node with a key/value pair that matches the key you were given 
 
 ### Methods
 - **set()**
 - **get()**: Takes in key, gets the hash, and goes to the index location specified. 
 - **has()**: Accepts a key and returns a bool on if that key exists inside the hashtable.
 - **keys()**: Returns a collection (array) of unique hash keys.
 - **hash()**: Accepts a key as a string, conducts the hash, and returns index of array where the key/value should be placed.
