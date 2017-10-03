### Number Complement
#### 题目：
Given a positive integer, output its complement number. The complement strategy is to flip the bits of its binary representation.

#### 翻译：
给定一个正整数，输出它的补码，补码的策略是转换它的二进制的位

#### Example：
```
Input: 5
Output: 2
Explanation: The binary representation of 5 is 101 (no leading zero bits), and its complement is 010. So you need to output 2.
```
```
Input: 1
Output: 0
Explanation: The binary representation of 1 is 1 (no leading zero bits), and its complement is 0. So you need to output 0.
```

#### Note:

- The given integer is guaranteed to fit within the range of a 32-bit signed integer.
- You could assume no leading zero bit in the integer’s binary representation.


#### 解题思路
求他的补码，其实我们可以将这个整数转化成一个二进制的数，所以我们可以调用JS的一个接口toString，得到这个二进制的字符串之后，我们可以给一个循环，然后，根据这个循环，将这个二进制的数中的1和0反一反，最后将得到的结果，转化成一个我们想要的结果，调用的接口是parseInt(res, 2);

#### 代码实现
```
/**
 * @param {number} num
 * @return {number}
 */
var findComplement = function(num) {
    let numStr = num.toString(2),
        i = 0,
        numAll = '';
    for(;i < numStr.length; i++){
        numAll += parseInt(numStr[i]) ? '0' : '1';
    }
    return parseInt(numAll, 2);
};
```