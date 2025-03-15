## Corner cases[​](https://www.techinterviewhandbook.org/algorithms/string/#corner-cases "Direct link to Corner cases")
- Empty string
- String with 1 or 2 characters
- String with repeated characters
- Strings with only distinct characters

## Techniques

### Counting characters
Often you will need to count the frequency of characters in a string using a hash table/map.
If you need to keep a counter of characters, a common mistake is to say that the space complexity required for the counter is O(n). The space required for a counter of a string of latin characters is O(1) not O(n). This is because the upper bound is the range of characters, which is usually a fixed constant of 26.

#### String of unique characters[​](https://www.techinterviewhandbook.org/algorithms/string/#string-of-unique-characters "Direct link to String of unique characters")

A neat trick to count the characters in a string of unique characters is to use a 26-bit bitmask to indicate which lower case latin characters are inside the string.

```
mask = 0for c in word:  mask |= (1 << (ord(c) - ord('a')))
```

To determine if two strings have common characters, perform `&` on the two bitmasks. If the result is non-zero, ie. `mask_a & mask_b > 0`, then the two strings have common characters.



### Anagram

To determine if two strings are anagrams, there are a few approaches:

- Sorting both strings should produce the same resulting string. This takes O(n.log(n)) time and O(log(n)) space.
- If we map each character to a prime number and we multiply each mapped number together, anagrams should have the same multiple (prime factor decomposition). This takes O(n) time and O(1) space. Examples: [Group Anagram](https://leetcode.com/problems/group-anagrams/)
- Frequency counting of characters will help to determine if two strings are anagrams. This also takes O(n) time and O(1) space.

### Palindrome

Here are ways to determine if a string is a palindrome:

- Reverse the string and it should be equal to itself.
- Have two pointers at the start and end of the string. Move the pointers inward till they meet. At every point in time, the characters at both pointers should match.


When a question is about counting the number of palindromes, a common trick is to have two pointers that move outward, away from the middle. Note that palindromes can be even or odd length. For each middle pivot position, you need to check it twice - once that includes the character and once without the character. This technique is used in [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/).

- For substrings, you can terminate early once there is no match
- For subsequences, use dynamic programming as there are overlapping subproblems. Check out [this question](https://leetcode.com/problems/longest-palindromic-subsequence/)

## Essential questions[​](https://www.techinterviewhandbook.org/algorithms/string/#essential-questions "Direct link to Essential questions")

_These are essential questions to practice if you're studying for this topic._

- [Valid Anagram](https://leetcode.com/problems/valid-anagram)
- [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
- [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)

## Recommended practice questions[​](https://www.techinterviewhandbook.org/algorithms/string/#recommended-practice-questions "Direct link to Recommended practice questions")

_These are recommended questions to practice after you have studied for the topic and have practiced the essential questions._

- [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/)
- [Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string)
- [Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/description/)
- [Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- [Encode and Decode Strings (LeetCode Premium)](https://leetcode.com/problems/encode-and-decode-strings/)

testing

test1
