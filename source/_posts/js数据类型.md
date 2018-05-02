---
title: js数据类型
date: 2018-04-28 09:23:44
categories:
- js  
---
# 数据类型
在 JavaScript 中有 5 种不同的数据类型：

	string
	number
	boolean
	object
	function
3 种对象类型：

	Object
	Date
	Array
2 个不包含任何值的数据类型：

	null
	undefined
请注意

	NaN 的数据类型是 number
	数组(Array)的数据类型是 object
	日期(Date)的数据类型为 object
	null 的数据类型是 object
	未定义变量的数据类型为 undefined
JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：

	var x;               // x 为 undefined
	var x = 5;           // 现在 x 为数字
	var x = "John";      // 现在 x 为字符串
## 1. 简单数据类型
### 1.1 数字
JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：

	var x1=34.00;      //使用小数点来写
	var x2=34;         //不使用小数点来写
### 1.2 字符串
字符串可以是引号中的任意文本。您可以使用单引号或双引号：

	var carname="Volvo XC60";
	var carname='Volvo XC60';

你可以使用索引位置来访问字符串中的每个字符：

	var carname = carname[7];
字符串的索引从 0 开始，这意味着第一个字符索引值为 [0],第二个为 [1], 以此类推。

字符串长度

可以使用内置属性 length 来计算字符串的长度：
	
	var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
	var sln = txt.length;
### 1.3 布尔
只有2个值一个是true, 一个是false.   实际运算中true=1,false=0

	var x=true;
	var y=false;
### 1.4 undefined    
在 JavaScript 中, undefined 是一个没有设置值的变量。

typeof 一个没有值的变量会返回 undefined。

你可以设置为 undefined 来清空对象:

	var n;
	alert(n);
变量在内存中是存在的
### 1.5 null 
在 JavaScript 中 null 表示 "什么都没有"。

null是一个只有一个值的特殊类型。表示一个空对象引用。

你可以设置为 null 来清空对象:

	var n = 1;
	n = null;
	alert(n);
在内存中找不到这个变量
## 2. 复杂数据类型
### 2.1 JavaScript 数组
创建名为 cars 的数组：

	var cars=new Array();
	cars[0]="Saab";
	cars[1]="Volvo";
	cars[2]="BMW";
或者 (condensed array):

	var cars=new Array("Saab","Volvo","BMW");
或者 (literal array):

	var cars=["Saab","Volvo","BMW"];
### 2.2 JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

	var person={
		firstname : "John",
		lastname  : "Doe",
		id        :  5566
	};
上面例子中的对象 (person) 有三个属性：firstname、lastname 以及 id。

对象属性有两种寻址方式：

	name=person.lastname;
	name=person["lastname"];

### 2.3 对象方法属性的调用
	var person = {
	    firstName: "John",
	    lastName : "Doe",
	    id : 5566,
	    fullName : function() 
		{
	       return this.firstName + " " + this.lastName;
	    }
	};
person.fullName; //不加括号输出函数表达式 

	function () { return this.firstName + " " + this.lastName; }
person.fullName(); //加括号输出函数执行结果
	
	John Doe
### 3.判断数据类型

	typeof "John"                // 返回 string 
	typeof 3.14                  // 返回 number
	typeof false                 // 返回 boolean
	typeof [1,2,3,4]             // 返回 object
	typeof {name:'John', age:34} // 返回 object
在JavaScript中，数组是一种特殊的对象类型。 因此 typeof [1,2,3,4] 返回 object

	typeof undefined             // undefined
	typeof null                  // object
	null === undefined           // false
	null == undefined            // true
null 和 undefined 的值相等，但类型不等