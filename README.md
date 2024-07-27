# Minimum Cost to Convert String I

LeetCode Q # 2976.

You are given two 0-indexed strings source and target, both of length n and consisting of lowercase English letters. You are also given two 0-indexed character arrays original and changed, and an integer array cost, where cost[i] represents the cost of changing the character original[i] to the character changed[i].

You start with the string source. In one operation, you can pick a character x from the string and change it to the character y at a cost of z if there exists any index j such that cost[j] == z, original[j] == x, and changed[j] == y.

Return the minimum cost to convert the string source to the string target using any number of operations. If it is impossible to convert source to target, return -1.

Note that there may exist indices i, j such that original[j] == original[i] and changed[j] == changed[i].

Example 1:

> Input: source = "abcd", target = "acbe", original = ["a","b","c","c","e","d"], changed = ["b","c","b","e","b","e"], cost = [2,5,5,1,2,20]</br>
> Output: 28</br>
> Explanation: To convert the string "abcd" to string "acbe":</br>
> - Change value at index 1 from 'b' to 'c' at a cost of 5.</br>
> - Change value at index 2 from 'c' to 'e' at a cost of 1.</br>
> - Change value at index 2 from 'e' to 'b' at a cost of 2.</br>
> - Change value at index 3 from 'd' to 'e' at a cost of 20.</br>
> The total cost incurred is 5 + 1 + 2 + 20 = 28.</br>
> It can be shown that this is the minimum possible cost.</br>

Example 2:

> Input: source = "aaaa", target = "bbbb", original = ["a","c"], changed = ["c","b"], cost = [1,2]</br>
> Output: 12</br>
> Explanation: To change the character 'a' to 'b' change the character 'a' to 'c' at a cost of 1, followed by changing the character 'c' to 'b' at a cost of 2, for a total cost of 1 + 2 = 3. To change all occurrences of 'a' to 'b', a total cost of 3 * 4 = 12 is incurred.

Example 3:

> Input: source = "abcd", target = "abce", original = ["a"], changed = ["e"], cost = [10000]</br>
> Output: -1</br>
> Explanation: It is impossible to convert source to target because the value at index 3 cannot be changed from 'd' to 'e'.

My Solution Analysis:

<div align = "center">

  ![image](https://github.com/user-attachments/assets/c472720d-145c-4bc2-8cd8-3f77fa2e1916)

  Time complexity: O(26^3).</br>Space complexity: O(26^2).
</div>
