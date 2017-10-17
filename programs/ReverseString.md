### 题目
Write a function that takes a string as input and returns the string reversed.

### 翻译
写一个函数，将输入的字符串转化为反转的字符串

### Example
```
Given s = "hello", return "olleh".
```

### 实现思路
这个只要将字符串先分割到一个数组中，然后将数组倒置，在拼接起来

### 代码实现

```js
/**
 * @param {string} s
 * @return {string}
 */
var reverseString = function(s) {
    const arr = s.split(''),
          res = arr.reverse();
    return res.join('');
};
```