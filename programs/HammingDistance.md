### Hamming Distance

题目：
The Hamming distance between two integers is the number of positions at which the corresponding bits are different.
Given two integers x and y, calculate the Hamming distance.

翻译：
两个整数之间的Hamming距离是相应位不同的位置数。给定两个整数x和y，计算汉明距离。

Example:
```
Input: x = 1, y = 4
Output: 2;
Explanation:
1   (0 0 0 1)
4   (0 1 0 0)
不同位数是两位
```

解题思路：
你要如何去统计位数上的数是不相同的，语言本身就给我们提供了很好的方法——异或<br/>
异或，就是将位数不相同的为1，相同的标记为0

代码实现：
```js
/**
 * @param {number} x
 * @param {number} y
 * @return {number}
 */
var hammingDistance = function(x, y) {
    let num = x ^ y,
    str = num.toString(2),
    arr = str.split(''),
    i = 0;
    arr.forEach((index) => {
        if(index === '1') {
            i++;
        }
    });
    return i;
};
```