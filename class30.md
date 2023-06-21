<!-- Implementation: Hash Tables
To turn in your reading “Reply” to this discussion by teaching something that you learned from the readings listed below.

Some ideas for how you might want to teach:

Use an analogy
Explain a detail in depth
Use WHY, WHAT, HOW structure
Tutorial / walk through an example
Write a quiz
Create a vocabulary/definition list
Write a cheat sheet
Create a diagram / visualization / cartoon of a topic
Anthropomorphize the concepts, and write a conversation between them
Build a map of the information
Construct a fill-in-the-blank worksheet for the topic
Resources
Read Intro to Hash Tables
Watch what is a hash table?
Read basics of hash tables
Skim hash table wiki -->

# Hash Tables

## What is a hash table?

A hash table is a data structure that maps keys to values for highly efficient lookup. There are a number of ways to implement this, but the most common is to use an array of linked lists and a hash code function.

## What is a hash code function?

A hash code function is a function that takes a key and returns an index into the array.

## What makes a good hash code function?

A good hash code function satisfies two basic requirements:

1. It uses the data in the key to compute a hash code, and

2. It returns the same hash code when given the same key.

## Why is a good hash code function important?

A good hash code function can avoid collisions, which occur when two keys map to the same index. Collisions are bad because they cause two or more keys to be stored in the same slot of the hash table, which means that lookup might fail.

## What is a collision?

A collision occurs when two keys map to the same index in the array. In a good hash table, collisions should be rare, but they are not always avoidable.

## How are collisions handled?

There are two common ways to handle collisions: chaining and open addressing. Chaining means that each slot in the hash table holds a reference to a linked list of keys that have hashed to that slot. Open addressing means that when a collision occurs, we search through alternate locations in the array until we find an empty slot.

## example

```py
class HashTable:
    def __init__(self):
        self.MAX = 100
        self.arr = [[] for i in range(self.MAX)]

    def get_hash(self, key):
        h = 0
        for char in key:
            h += ord(char)
        return h % self.MAX

    def __getitem__(self, index):
        h = self.get_hash(index)
        for element in self.arr[h]:
            if element[0] == index:
                return element[1]

    def __setitem__(self, key, val):
        h = self.get_hash(key)
        found = False
        for idx, element in enumerate(self.arr[h]):
            if len(element) == 2 and element[0] == key:
                self.arr[h][idx] = (key, val)
                found = True
                break
        if not found:
            self.arr[h].append((key, val))

    def __delitem__(self, key):
        h = self.get_hash(key)
        for index, element in enumerate(self.arr[h]):
            if element[0] == key:
                del self.arr[h][index]

```

## Resources

- [Hash Tables 1](https://www.youtube.com/watch?v=KyUTuwz_b7Q)
- [Hash Tables 2](https://www.youtube.com/watch?v=shs0KM3wKv8)
- [Hash Tables practice](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
