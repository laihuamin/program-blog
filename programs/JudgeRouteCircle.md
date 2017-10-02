## Judge Route Circle


题目：
Initially, there is a Robot at position (0, 0). Given a sequence of its moves, judge if this robot makes a circle, which means it moves back to the original place.

The move sequence is represented by a string. And each move is represent by a character. The valid robot moves are R (Right), L (Left), U (Up) and D (down). The output should be true or false representing whether the robot makes a circle.

翻译：
机器人的起始位置是(0, 0)，给机器人一系列的行动，判断机器人是否在画一个圆，意思就是这一系列的行动能不能回到原始的位置

这一系列的行为是一个字符串，每一个移动行为是字符串中的一个字母，机器人的有效行动是上、下、左、右，输出的值是false和true，代表机器人能否画一个圆。

解题思路：
能否回到原点这是一个关键点，回到原点的条件是什么，上下步数一致，左右步数一致，既然要步数一致，那么我们就需要左右，上下各用一个数来表示，上右为加一，反之减一，根据最后这个数的值来判断false和true

Example1：
```js
Input: "UD"
Output: true
```
Example2
```js
Input: "LL"
Output: false
```

代码实现：
```js
/**
 * @param {string} moves
 * @return {boolean}
 */
var judgeCircle = function(moves) {
    const arr = moves.split('');
    const res = {};
    let alignIndex = 0,
        vertIndex = 0,
        i = 0;
    for(;i < arr.length; i++){
        switch(arr[i])
        {
            case 'L':
                alignIndex--;
                break;
            case 'R':
                alignIndex++;
                break;
            case 'U':
                vertIndex++;
                break;
            case 'D':
                vertIndex--;
                break;
            default:
                break;
        }
    }
    return vertIndex !== 0 || alignIndex !== 0 ? false : true; 
};
```