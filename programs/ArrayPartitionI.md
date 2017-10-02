### Array Partition I

#### 题目：
Given an array of 2n integers, your task is to group these integers into n pairs of integer, say (a1, b1), (a2, b2), ..., (an, bn) which makes sum of min(ai, bi) for all i from 1 to n as large as possible.

#### 翻译：
给定一个2n的整数数组，你的任务是将这个数组分成n对数组，比如(a1,b1),(a2,b2)...(an,bn),使得数组(ai,bi)在1到n的数组中尽可能的大

#### example：

```
Input: [1,4,3,2]

Output: 4
Explanation: n is 2, and the maximum sum of pairs is 4 = min(1, 2) + min(3, 4).
```

#### Note:

- n is a positive integer, which is in the range of [1, 10000].
- All the integers in the array will be in the range of [-10000, 10000].


#### 解题思路：
其实这题来说很简单，我们只要明白这题的需求是什么，第一、后面的数尽可能的到，那么我们可以理解为，在两两切分数组的时候，我们应该先排序，第二、我们是否有必要切分数组，没必要，因为我们可以在排完序后，将这个数组的下标为偶数为的数组相加，就是我们要得到的结果，为什么呢？因为当你两两切割之后，永远是前面一位比后面的小

#### 代码实现
```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var arrayPairSum = function(nums) {
    nums.sort((item1,item2) => item1 - item2);
    let sum = 0;
    nums.forEach((value, index) => {
        if(index % 2 === 0){
            sum += value;
        }
    });
    return sum;
};
```