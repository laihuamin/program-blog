## python学习教程
```py
# _*_ coding: utf-8 _*_  中文用户一般得先用这一行来声明变量
import os  # 导入其他模块名

def main()  #函数名‘main’在这里不是必须的，调用在脚本的最后一部分
    #最好的编程习惯是：一般在前面缩进4个空格
    print 'hello world'  #打印一个hello world
    print "这是Alice\'问候" #声明字符串，单双引号都可以，但是要对字符串中的单引号做转意处理
    print '这是Bob\'问候'

    foo(5, 10) #调用后面声明的函数

    print '=' * 10 #符号可乘，会输出‘==========’
    print '这里直接执行'+os.cwd() #加号起到连接字符串的作用，后面是调用os中的函数式

    counter = 0 #变量得先实例化才能计算
    counter += 1

    food = ['香蕉', '橘子', '苹果', '梨'] #内置列表的数据对象，可以是不同的数据类型，也可以是不同的列表对象
    for i in food: #i指代列表中按顺序的每一个food,注意for in语句循环需要用冒号结束
        print '水果'+i #每换一层逻辑，缩进一级，可以使得逻辑更加清晰

    print '数到10'
    for i in range(10): #range(10)就相当于[0.1,2,3,4,5,6,7,8,9]的数字列表
        print i

def foo(param1, secondParam): #函数式声明注意冒号结束声明
    result = param1+secondParam #字符串格式书写类似c语言
    print '%s 加 $s 等于 %s' %(param1, secondParam, result)

    if result < 50: #声明结束用冒号，判定式于c语言一样
        print '这个'
    elif (result > 50) and ((param1 == 42) or (secondParam == 24)):  #逻辑运算符用更加直观的英文
        print '那个'
    else:
        print 'this'
    return result #这里是单行注释
    '''这里是
多行注释·····'''

if __name__=='__main__':
    main()

```
