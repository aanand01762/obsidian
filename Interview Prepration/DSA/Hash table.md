In the case of hash collisions, there are a number of collision resolution techniques that can be used. You will unlikely be asked about details of collision resolution techniques in interviews:

- **Separate chaining** - A linked list is used for each value, so that it stores all the collided items.
- **Open addressing** - All entry records are stored in the bucket array itself. When a new entry has to be inserted, the buckets are examined, starting with the hashed-to slot and proceeding in some probe sequence, until an unoccupied slot is found.


## Learning resources[​](https://www.techinterviewhandbook.org/algorithms/hash-table/#learning-resources "Direct link to Learning resources")

- Readings
    - [Taking Hash Tables Off The Shelf](https://medium.com/basecs/taking-hash-tables-off-the-shelf-139cbf4752f0), basecs
    - [Hashing Out Hash Functions](https://medium.com/basecs/hashing-out-hash-functions-ea5dd8beb4dd), basecs
- Videos
    - [Core: Hash Tables](https://www.coursera.org/lecture/data-structures-optimizing-performance/core-hash-tables-m7UuP), University of California San Diego
    - [A Brief Guide to Hash Tables](https://www.youtube.com/watch?v=r1XZGP5ppqQ) ([slides](https://samuelalbanie.com/files/digest-slides/2022-09-brief-guide-to-hash-tables.pdf)), Samuel Albanie, University of Cambridge

## Sample questions[​](https://www.techinterviewhandbook.org/algorithms/hash-table/#sample-questions "Direct link to Sample questions")

- Describe an implementation of a least-used cache, and big-O notation of it.
- A question involving an API's integration with hash map where the buckets of hash map are made up of linked lists.

## Essential questions[​](https://www.techinterviewhandbook.org/algorithms/hash-table/#essential-questions "Direct link to Essential questions")

_These are essential questions to practice if you're studying for this topic._

- [Two Sum](https://leetcode.com/problems/two-sum)
- [Ransom Note](https://leetcode.com/problems/ransom-note)

## Recommended practice questions[​](https://www.techinterviewhandbook.org/algorithms/hash-table/#recommended-practice-questions "Direct link to Recommended practice questions")

_These are recommended questions to practice after you have studied for the topic and have practiced the essential questions._

- [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- [Insert Delete GetRandom O(1)](https://leetcode.com/problems/insert-delete-getrandom-o1/)
- [First Missing Positive](https://leetcode.com/problems/first-missing-positive/)
- [LRU Cache](https://leetcode.com/problems/lru-cache/)
- [All O one Data Structure](https://leetcode.com/problems/all-oone-data-structure/)