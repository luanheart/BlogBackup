---
layout: post
title: javascript笔记杂谈
category: javascript
---

js中的区块和大多数的语言不一样，在块里定义外面仍可访问

```javascript
{
  var a = 1;
}
a	//1
```

js可分为6种数据类型(number, string, boolean, undefined, null, object)，ES6加入第七种Symbol类型的值。

object还可以分成

> 狭义的对象（object）
>
> 数组（array）
>
> 函数（function）



空数组（[]）和空对象（{}）对应的布尔值都是true



### String 对象

#### 1. concat()

`concat`方法连接两个字符串，并返回一个新的字符串，不改变原字符串

```
var s1 = 'abc';
var s2 = 'def';

s1.concat(s2) // "abcdef"
s1 // "abc"
```

该方法可以接受多个参数。

```
'a'.concat('b', 'c') // "abc"

```

如果参数不是字符串，`concat`方法会将其先转为字符串，然后再连接。

```
var one = 1;
var two = 2;
var three = '3';

''.concat(one, two, three) // "123"
one + two + three // "33"

```

上面代码中，`concat`方法将参数先转成字符串再连接，所以返回的是一个三个字符的字符串。作为对比，加号运算符在两个运算数都是数值时，不会转换类型，所以返回的是一个两个字符的字符串。