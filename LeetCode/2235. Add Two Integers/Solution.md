# 2235. Add Two Integers

---

## Intuition

The most straightforward approach is to simply return num1 + num2.

---

## Approach

The approach chosen is a direct summation using a function, which is the most direct and least error-prone method for this task.

---

## Complexity

- Time complexity: O(1) - as the sum operation is a constant time operation.

- Space complexity: O(1) - no additional space is used, the space required does not depend on the size of the input numbers.

---

## Code

```C++
class Solution {
public:
    int sum(int num1, int num2) {
        return num1 + num2;
    }
};
```
