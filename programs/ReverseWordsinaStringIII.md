### 题目

Given a string, you need to reverse the order of characters in each word within a sentence while still preserving whitespace and initial word order.

### 翻译

给定一个字符串，您需要在一个句子中对每个单词的字符顺序进行反向转换，同时保留空格和初始单词顺序。

### Example 1:

```
Input: "Let's take LeetCode contest"
Output: "s'teL ekat edoCteeL tsetnoc"
```

### 解题思路

其实这题很简单，将整个句子分割成每一个单词，然后循环遍历每一个单词，对每一个单词做切割，反转，在组合。最后在将整个数组整合，之后输出

### 代码实现

```js
/**
 * @param {string} s
 * @return {string}
 */
var reverseWords = function(s) {
    const arr = s.split(' ');
    for(let i = 0; i < arr.length; i++) {
        let temp = arr[i].split(''),
            res = temp.reverse();
        arr[i] = res.join('');
    }
    return arr.join(' ');
};
```

### 代码时耗

![Reverse Words in a String III](http://laihuamin.oss-cn-beijing.aliyuncs.com/ReverseWordsInAString-III.png)