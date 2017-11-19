# Python的基本类型

## Number 数字

`int`, `float`, `bool`, `complex`

### int 和 float
- 整数： int （无short,int,long）
- 浮点数： float（无单精度和双精度之分）

1. 验证

```py
type(1) ===> int
type(-1) ===> int
type(1.1) ===> float
type(1 + 0.1) ===> float
type(1 + 1.0) ===> float
type(1 * 1) ==> int
type(1 * 1.0) ===> float
type(2 / 2) ===> float （整数除以整数，得浮点数）1.0
type(2 // 2) ===> int 1
1//2 ===> 0
// ：整除 ，  / ：除法，自动转型为浮点数
```
2. 进制简介：

10进制，2进制，8进制，16进制
10进制： 满十进一
2进制： 满二进一 0, 1, 10
8进制： 0, 1, 2, 3, 4, 5, 6, 7, 10
16进制： 0, 1, 2 ... 9, A, B, C, D, E, F, 10

3. 进制的表示：

0b前缀表示二进制（在编译器直接输入比如0b10，结果为2。自动转化为10进制）

0o前缀表示八进制（0o10 ===> 8）

0x前缀表示16进制（0x10 ===> 16）

其它进制转为其它进制：（使用python的方法）

转为二进制： bin()
转为十进制： int()
转为十六进制： hex()
转为八进制： oct()

### bool和complex

- bool 布尔类型： 真、假
- complex 复数

1. bool

True  False

``` py
type(True) ===> bool
int(True) ===> 1
int(False) ===> 0
```

非零的数值都表示bool真：

``` py
bool(1) ===> True
bool(0) ===> False
bool(2) ===> True
bool(0b0) ===> False
bool('abc) ===> True
bool('') ===> False
列表：
bool([1,2,3]) ===> True
bool([]) ===> False

bool({}) ===> False
bool(None) ===> False
```
2. complex

复数：36j 就表示复数

## 序列

### str字符串

1. 表示：

- 单引号：

``` py
'hello world'
'let's go'（报错）
'let"s go'
'let\'s go' (转义字符)
```

- 双引号：

``` py
"hello world"
"let's go"
```

- 三引号：

多行字符串

``` py
'''
hello
hello
'''
或者
"""
hello
hello
"""
输出效果是：
'\nhello\nhello\n'
```

``` py
输入：
'''hello world\nhello world\nhello world'''
无效果
输入：
print('''hello world\nhello world\nhello world''')
print('hello world\nhello world\nhello world')
出现换行效果
```

``` py
'hello\
world'
输出'helloworld'
```

2. 转义字符

\n 换行
\' 单引号
\t 横向制表符
\r 回车

``` py
print('hello \\n world')
输出：hello \n world
```

3. 原始字符串

``` py
输入：print(r'c:\northwind\northwest')
输出：
c:\northwind\northwest

不是一个普通字符串而是一个原始字符串

输入：
print(r'let's go')  报错
应该输入print(r"let's go")
```

4. 字符串运算

``` py
'hello' + 'world' ===> 'helloworld'

'hello' * 3 ===> 'hellohellohello'

'hello world'[0] ===> 'h'

'hello world'[-1] ===> 'd'

'hello world'[0:5] ===> 'hello'

'hello world'[0:-1] ===> 'hello worl'

'hello world'[6:11] ===> 'world'

'hello world'[6:] ===>  'world'
```
