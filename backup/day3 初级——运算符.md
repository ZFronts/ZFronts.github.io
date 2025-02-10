`部分内容基于菜鸟教程的《运算符》部分，同时拓展了一些点`
# 一、算术运算符：

![Image](https://github.com/user-attachments/assets/5ce7e3cc-4971-4821-a57b-fb03083e0dcd)
举例：
```python
a = 2;b = -5
print(f'{a} + {b} = {a + b}')
print(f'{a} - {b} = {a - b}')
print(f'{a} * {b} = {a * b}')
print(f'{a} / {b} = {a / b}')
print(f'{a} % {b} = {a % b}')
print(f'{a} ** {b} = {a ** b}')
print(f'{a} // {b} = {a // b}')

# 2 + -5 = -3
# 2 - -5 = 7
# 2 * -5 = -10
# 2 / -5 = -0.4
# 2 % -5 = -3 —— 2%-5=2-(-5)*(-1)=2-5=-3
# 2 ** -5 = 0.03125
# 2 // -5 = -1

a = -2;b = 5
print(f'{a} + {b} = {a + b}')
print(f'{a} - {b} = {a - b}')
print(f'{a} * {b} = {a * b}')
print(f'{a} / {b} = {a / b}')
print(f'{a} % {b} = {a % b}')
print(f'{a} ** {b} = {a ** b}')
print(f'{a} // {b} = {a // b}')

# -2 + 5 = 3
# -2 - 5 = -7
# -2 * 5 = -10
# -2 / 5 = -0.4
# -2 % 5 = 3 —— -2%5=-2-5*(-1)=-2+5=3
# -2 ** 5 = -32
# -2 // 5 = -1
```
# 二、（二进制）位运算符：
## 1、注意：
- 如果数据为非二进制数据，计算机将把数据<ins>自动转成**二进制**</ins>再进行计算；
- 生活中通常使用**8位二进制**，在程序中则不受位数限制（在超过最大数以前）
## 2、运算符表：

![Image](https://github.com/user-attachments/assets/184a147a-4d43-4366-b06f-dc56837ca1b1)

举例：
```python
a = 60            # 60 = (0) 0011 1100 —— (0)为符号位，表示为正数
b = 13            # 13 = 0000 1101 
c = 0
 
c = a & b        # 12 = 0000 1100
print ("1 - c 的值为：", c)
 
c = a | b        # 61 = 0011 1101 
print ("2 - c 的值为：", c)
 
c = a ^ b        # 49 = 0011 0001
print ("3 - c 的值为：", c)
 
c = ~a           # -61 = (1) 1100 0011 —— (1)为符号位，表示为负数，-61 = (1100 0011)代表的正十进制数195 -256【8位2进制的情况下】
 print ("4 - c 的值为：", c)
 
c = a << 2       # 240 = 1111 0000
print ("5 - c 的值为：", c)
 
c = a >> 2       # 15 = 0000 1111
print ("6 - c 的值为：", c)
```
# 三、赋值运算符：
## 1、运算符表：

![Image](https://github.com/user-attachments/assets/ddae3cb5-e52b-4a78-a52f-8e78b76cfedc)

## 2、特点：
- 结合性：<ins>**从右往左**</ins>；
- 支持<ins>**链式赋值**</ins>：e.g.a=b=c=20（id相同）；
- 支持<ins>**参数赋值**</ins>：即支持+=、-=、*=、/=、//=、%=、**=、<<=、>>=、&=、|=、^=；
- 支持<ins>**系列解包赋值**</ins>：e.g.a，b，c=20，30，40；`通过这个特点可简单实现交换变量：a，b=10，20;a，b=b，a;`
## 3、海象运算符：
参考[菜鸟教程](https://www.runoob.com/python3/python3-basic-operators.html)
- 主要目的：在表达式中<ins>**同时进行赋值和返回赋值的值**</ins>
- 实际意义：使用海象运算符可以在一些情况下简化代码，尤其是**在需要在表达式中使用赋值结果的情况下**。这对于简化循环条件或表达式中的重复计算很有用；
- 实例：
```python
# 传统写法
n = 10
if n > 5:
    print(n)

# 使用海象运算符
if (n := 10) > 5:
    print(n)
```

![Image](https://github.com/user-attachments/assets/36385661-bcc3-402e-aba5-508dde0f1c08)

- 优点：
  - 海象运算符（:=）允许在表达式内部进行赋值，这可以减少代码的重复，提高代码的可读性和简洁性。
  - 在上述例子中，传统写法需要单独一行来赋值 n，然后在 if 语句中进行条件检查。而使用海象运算符的写法可以在 if 语句中直接进行赋值和条件检查。

`海象运算符的理解也可以参考博客：`[深入浅出理解海象运算符:=](https://blog.csdn.net/weixin_43483381/article/details/104084404)
# 四、比较运算符：	
## 1、运算符表：

![Image](https://github.com/user-attachments/assets/8a219d24-115e-426d-b1af-d6b5242167c2)

## 2、特点：
- 支持<ins>**链式比较**</ins>，例如`a<b<c、a>b>c、a<b>c、a>b<c、a<b==c、a!=b>c等……`
- 链式比较<ins>**隐含and运算符**</ins>>，例如a<b<c等价于(a<b) and (b<c)
# 五、逻辑（布尔）运算符：
## 1、运算符表
![Image](https://github.com/user-attachments/assets/2df9d684-fa0b-4e51-abd7-6d9ad566b598)
## 2、注意：
and 和 or 具有<ins>**短路**</ins>性质；
- and的短路：当and左侧值为False时，不去计算右侧的值而直接返回False
- or的短路：当or左侧值为True时，不去计算右侧的值而直接返回True
```python
a, b, c, d, m, n = 5, 6, 7, 8, 2, 2
print((m:=a)>b and (n:=c)>d)
print(f'm = {m}, n = {n}')

# 重置m
m = 2
print(f'm = {m}, n = {n}')

print((m:=a)<b or (n:=c)>d)
print(f'm = {m}, n = {n}')

# False
# m = 5, n = 2
# m = 2, n = 2
# True
# m = 5, n = 2
```
## 3、举例：
```python
a = 10
b = 20

print(f'{a} and {b} = {a and b}')
print(f'{a} or {b} = {a or b}')

# 修改变量 a 的值
a = 0
print(f'{a} and {b} = {a and b}')
print(f'{a} or {b} = {a or b}')
print(f'not {a} = {not a}')
print(f'not {b} = {not b}')

# 10 and 20 = 20
# 10 or 20 = 10
# 0 and 20 = 0
# 0 or 20 = 20
# not 0 = True
# not 20 = False
```
# 六、成员运算符：	

![Image](https://github.com/user-attachments/assets/68a72741-de78-4ccf-817d-bc89321e88cb)

举例：
```python
#!/usr/bin/python3

a = 10
b = 20
list = [1, 2, 3, 4, 5]

if (a in list):
    print("1 - 变量 a 在给定的列表中 list 中")
else:
    print("1 - 变量 a 不在给定的列表中 list 中")

if (b not in list):
    print("2 - 变量 b 不在给定的列表中 list 中")
else:
    print("2 - 变量 b 在给定的列表中 list 中")

# 修改变量 a 的值
a = 2
if (a in list):
    print("3 - 变量 a 在给定的列表中 list 中")
else:
    print("3 - 变量 a 不在给定的列表中 list 中")
    
# 1 - 变量 a 不在给定的列表中 list 中
# 2 - 变量 b 不在给定的列表中 list 中
# 3 - 变量 a 在给定的列表中 list 中
```
# 七、身份运算符：
## 1、运算符表：

![Image](https://github.com/user-attachments/assets/fd305c87-34ee-4766-b13f-519f4dcb0e7f)

## 2、is 与 == 区别：
is 用于判断两个变量引用对象是否为同一个， == 用于判断引用变量的值是否相等。
# 八、其它运算符：
## 1、绑定或加圆括号的表达式(expressions...)；
## 2、列表显示[expressions...]；
## 3、字典显示{key:value...}；
## 4、集合显示{expressions...}；
## 5、抽取（索引）x[index]；
## 6、切片x[index1:index2]；
## 7、调用x(arguments...)；
## 8、属性引用x.attribute；
## 9、await表达式await x：
用于<ins>**管理协程**</ins>，**不用掌握**。
## 10、条件运算符-- if -- else --：
- 类似于C/C++中的“?:”；
- 表达式`x if C else y`首先是对条件 C 而非 x 求值。 如果 C 为真，x 将被求值并返回其值；否则将对 y 求值并返回其值。
## 11、lambda表达式：
被用于<ins>**创建匿名函数**</ins>。 表达式`lambda parameters: expression`会产生一个**函数对象** 。 该未命名对象的行为类似于用以下方式定义的函数：
```python
def <lambda>(parameters):
    return expression
```
## 12、逗号运算符：
主要作用之一是<ins>**创建元组**</ins>。即使没有显式的圆括号，逗号也会将多个值组合成一个元组；
# 九、运算符优先级：
`勘误：赋值运算符中漏了个海象运算符`
![Image](https://github.com/user-attachments/assets/b109e8a4-5ccd-4eec-8bbc-74af9f076844)