# JAVA_ArrayList 知识

1. [声明ArrayList](#声明数组队列)
2. [添加元素](#添加元素)
3. [访问元素](#访问元素)
4. [修改元素](#修改元素)
5. [删除元素](#删除元素)
6. [计算大小](#计算大小)
7. [换行输出(迭代)数组列表](#换行输出数组列表)
8. [排序](#排序)


## 声明数组队列
    import java.util.ArrayList; // 使用前先引入
    
    ArrayList <E> objectname = new ArrayList <>(); // 初始化  

`E` ：数据类型，只能为引用数据类型
`objectname`：对象名

## 添加元素
添加元素到ArrayList可以使用`add()`方法

    ArrayList <String> sites = new ArrayList <>();
    sites.add("A");
    sites.add("B");
    sites.add("C");
    System.out.println(sites);

以上实例执行结果为：
[A,B,C]

**以下对元素的操作基于此实例**

## 访问元素
访问元素可以用`get()`方法

    System.out.println(sites.get(1)); // 访问第2个元素

执行结果：
    B

## 修改元素
`set()`方法

    sites.set(2,"D"); // 第一个为索引位置，第二个为要修改的值
    System.out.println(sites);
    

执行结果：
    [A,B,D]

## 删除元素
`remove()`方法

    sites.remove(1); //删除第二个元素
    System.out.println(sites);

执行结果：
    [A,C]

## 计算大小
计算ArrayList中的元素数量用 `size()`方法
    
    System.out.println(sites.size());

执行结果：
    3

## 换行输出数组列表
使用for遍历数组队列：

    for(int i = 0; i < sites.size(); i++){
        System.out.println(sites.get(i));
    }
也可使用for-each来迭代元素：

    for(String i : sites){
        System.out.println(i);
    }
以上实例执行结果：
A
B
C

## 排序
Collections 类也是一个有用的类，位于java.util中，提供的sort()方法可以对字符或数字列表进行排序

    java.util.Collections; // 引入Collections 类

    Collections.sort(sites); // 字母排序

    for(String i : sites){
        System.out.println(i);
    }
以上实例执行结果：
A
B
C

<!--
    以上均来自www.runoob.com
-->