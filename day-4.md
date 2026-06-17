# Day 4

Problem: 
leetcode link:

```js
function groupAnagrams(strs) {
  const map = {};
  for (let i = 0; i < strs.length; i++) {
    const key = strs[i].split('').sort().join('');
    if (map[key] === undefined) {
      map[key] = [];
    }
    map[key].push(strs[i]);
  }
  return Object.values(map);
}
```
Input: nums: List[integer]

Output: List[integer]

Algorith:


Python Solution:

```py
def groupAnagrams(strs):
    anagram_map = {}

    for word in strs:
        key = ''.join(sorted(word))

        if key not in anagram_map:
            anagram_map[key] = []

        anagram_map[key].append(word)

    return list(anagram_map.values())
```
