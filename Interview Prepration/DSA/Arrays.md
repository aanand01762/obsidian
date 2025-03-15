

## Things to look out for during interviews[​](https://www.techinterviewhandbook.org/algorithms/array/#things-to-look-out-for-during-interviews "Direct link to Things to look out for during interviews")

- Clarify if there are duplicate values in the array. Would the presence of duplicate values affect the answer? Does it make the question simpler or harder?
- When using an index to iterate through array elements, be careful not to go out of bounds.
- Be mindful about slicing or concatenating arrays in your code. Typically, slicing and concatenating arrays would take O(n) time. Use start and end indices to demarcate a subarray/range where possible.

## Corner cases[​](https://www.techinterviewhandbook.org/algorithms/array/#corner-cases "Direct link to Corner cases")

- Empty sequence
- Sequence with 1 or 2 elements
- Sequence with repeated elements [1, 2, 3], [3,2,1]
- Duplicated values in the sequence [1, 2, 2]

## Techniques[​](https://www.techinterviewhandbook.org/algorithms/array/#techniques "Direct link to Techniques")

Note that because both arrays and strings are sequences (a string is an array of characters), most of the techniques here will apply to string problems.

### Sliding window[​](https://www.techinterviewhandbook.org/algorithms/array/#sliding-window "Direct link to Sliding window")

Master the [sliding window technique](https://discuss.leetcode.com/topic/30941/here-is-a-10-line-template-that-can-solve-most-substring-problems) that applies to many subarray/substring problems. In a sliding window, the two pointers usually move in the same direction will never overtake each other. This ensures that each value is only visited at most twice and the time complexity is still O(n). Examples: [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/), [Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/), [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)

### Two pointers[​](https://www.techinterviewhandbook.org/algorithms/array/#two-pointers "Direct link to Two pointers")

Two pointers is a more general version of sliding window where the pointers can cross each other and can be on different arrays. Examples: [Sort Colors](https://leetcode.com/problems/sort-colors/), [Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/)

When you are given two arrays to process, it is common to have one index per array (pointer) to traverse/compare the both of them, incrementing one of the pointers when relevant. For example, we use this approach to merge two sorted arrays. Examples: [Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)

### Traversing from the right[​](https://www.techinterviewhandbook.org/algorithms/array/#traversing-from-the-right "Direct link to Traversing from the right")

Sometimes you can traverse the array starting from the right instead of the conventional approach of from the left. Examples: [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/), [Number of Visible People in a Queue](https://leetcode.com/problems/number-of-visible-people-in-a-queue/)

### Sorting the array[​](https://www.techinterviewhandbook.org/algorithms/array/#sorting-the-array "Direct link to Sorting the array")

Is the array sorted or partially sorted? If it is, some form of binary search should be possible. This also usually means that the interviewer is looking for a solution that is faster than O(n).

Can you sort the array? Sometimes sorting the array first may significantly simplify the problem. Obviously this would not work if the order of array elements need to be preserved. Examples: [Merge Intervals](https://leetcode.com/problems/merge-intervals/), [Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)

### Precomputation[​](https://www.techinterviewhandbook.org/algorithms/array/#precomputation "Direct link to Precomputation")

For questions where summation or multiplication of a subarray is involved, pre-computation using hashing or a prefix/suffix sum/product might be useful. Examples: [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/), [Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/), [LeetCode questions tagged "prefix-sum"](https://leetcode.com/tag/prefix-sum/)

### Index as a hash key[​](https://www.techinterviewhandbook.org/algorithms/array/#index-as-a-hash-key "Direct link to Index as a hash key")

If you are given a sequence and the interviewer asks for O(1) space, it might be possible to use the array itself as a hash table. For example, if the array only has values from 1 to N, where N is the length of the array, negate the value at that index (minus one) to indicate presence of that number. Examples: [First Missing Positive](https://leetcode.com/problems/first-missing-positive/), [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)

### Traversing the array more than once[​](https://www.techinterviewhandbook.org/algorithms/array/#traversing-the-array-more-than-once "Direct link to Traversing the array more than once")

This might be obvious, but traversing the array twice/thrice (as long as fewer than n times) is still O(n). Sometimes traversing the array more than once can help you solve the problem while keeping the time complexity to O(n).