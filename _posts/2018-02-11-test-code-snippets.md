---
layout: post
title:  "Java基础笔记（1）"
date:   2018-02-11
desc: "NOHING"
keywords: "AlexMYH"
categories: [Java]
tags: [AlexMYH,Java]
icon: icon-html
---

# 变量: #
1：局部变量声明后，必须初始化，才可以使用。
2：实例变量具有默认值。数值型变量的默认值是0，布尔型变量的默认值是false，引用类型变量的默认值是null。变量的值可以在声明时指定，也可以在构造方法中指定；
      （声明在一个类中，方法外）
3：类变量（静态变量）：以static关键字声明，必须在方法之外；
       数值型变量默认值是0，布尔型默认值是false，引用类型默认值是null（与实例变量一样）；
       变量的值可以在声明的时候指定，也可以在构造方法中指定。此外，静态变量还可以在静态语句块中初始化； 
       类变量被声明为public static final类型时，类变量名称必须使用大写字母。

# 访问修饰符： #
1：默认的，也称为default，在同一包内可见，不使用任何修饰符。
2：私有的，以private修饰符指定，只能在同一类内可见。
    (要用来隐藏类的实现细节和保护类的数据)
3：共有的，以public修饰符指定，对所有类可见。
4：受保护的，以protected修饰符指定，对同一包内的类和所有子类可见。
    父类中声明为public的方法在子类中也必须为public。
    父类中声明为protected的方法在子类中要么声明为protected，要么声明为public。不能声明为private。
    父类中默认修饰符声明的方法，能够在子类中声明为private。
    父类中声明为private的方法，不能够被继承。

# 非访问修饰符： #
1:static修饰符，用来创建类方法（静态方法）和类变量(静态变量）。
     局部变量不能被声明为static变量；
     静态方法不能使用类的非静态变量。
2:Final修饰符，用来修饰类、方法和变量。
     final修饰的类不能够被继承；
     声明final方法的主要目的是防止该方法的内容被修改；
     修饰的变量为常量，是不可修改的。
3:Abstract修饰符，用来创建抽象类和抽象方法。
     抽象类不能用来实例化对象，声明抽象类的唯一目的是为了将来对该类进行扩充；
     抽象方法是一种没有任何实现的方法，该方法的的具体实现由子类提供。
4:Synchronized和volatile修饰符，主要用于线程的编程。

# 运算符： #
1: 算术运算符
2: 逻辑运算符
3：位运算符
4：逻辑运算符
5：赋值运算符
6：条件运算符（三元运算符？：)
```
b = (a == 1) ? 20: 30;    
System.out.println( "Value of b is : " +  b );//若a==1为假，输出30
```

7：instanceOf运算符：
```
String name = 'James';
boolean result = name instanceOf String; // 由于name是Strine类型，所以返回真
```

# 循环语句： #
1：for 
```
for(初始化; 布尔表达式; 更新) {
          //代码语句
                              }
java增强for循环：for(声明语句 : 表达式)
        {
          //代码句子
               }//主要用于数组的增强型for循环
 ```

2:while
```
while( 布尔表达式 ) {
	   //循环内容
                }
```

3:do...while
```
do {
      //代码语句
      }while(布尔表达式);
```

4：break:     跳出最里层的循环，并且继续执行该循环下面的语句。
   continue:  作用是让程序立刻跳转到下一次循环的迭代。

# 数组： #

声明：
```
dataType[] arrayRefVar;   // 首选的方法
dataType arrayRefVar[];  // 效果相同，但不是首选方法
```

```      
例：double[] myList = new double[10]; //声明与创建
    取长度：myList.length
    取第二个数：myList[1]
```

---






























