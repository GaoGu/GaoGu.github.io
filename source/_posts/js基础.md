---
title: JS
categories:
- js  
---
# JavaScript输出消息
## 1.window的方法
### 1.1alert()  
显示带有一条指定消息和一个 确认 按钮的警告框，早期JS调试使用。
### 1.2confirm()  
在页面弹出一个对话框, 常配合if判断使用。

如果访问者点击"确定"，此方法返回true，否则返回false。

	if(confirm("你好")){
	    alert("确定");
	}else{
	    alert("取消");
	}
### 1.3prompt()
prompt()方法用于显示可提示用户进行输入的对话框。
这个方法返回用户输入的字符串。
## 2.JavaScript Console 对象
console.log()  

将信息输入到控制台，用于js调试

## 3.HTML DOM Document 对象
document.write()
在页面输出消息
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
在JavaScript中，数组是一种特殊的对象类型。 因此 typeof [1,2,3,4] 返回 object。

	typeof undefined             // undefined
	typeof null                  // object
	null === undefined           // false
	null == undefined            // true
null 和 undefined 的值相等，但类型不等：
# 语句
## 1. if...Else 语句
语法

	if (condition1)
	{
	    当条件 1 为 true 时执行的代码
	}
	else if (condition2)
	{
	    当条件 2 为 true 时执行的代码
	}
	else
	{
	  当条件 1 和 条件 2 都不为 true 时执行的代码
	}
例子

	if (time<10)
	{
	    document.write("<b>早上好</b>");
	}
	else if (time>=10 && time<16)
	{
	    document.write("<b>今天好</b>");
	}
	else
	{
	    document.write("<b>晚上好!</b>");
	}
## 2. switch 语句
语法

	switch(n)
	{
	    case 1:
	        执行代码块 1
	        break;
	    case 2:
	        执行代码块 2
	        break;
	    default:
	        与 case 1 和 case 2 不同时执行的代码
	}
例子

	var d=new Date().getDay(); 
	switch (d) 
	{ 
	  case 0:x="今天是星期日"; 
	  break; 
	  case 1:x="今天是星期一"; 
	  break; 
	  case 2:x="今天是星期二"; 
	  break; 
	  case 3:x="今天是星期三"; 
	  break; 
	  case 4:x="今天是星期四"; 
	  break; 
	  case 5:x="今天是星期五"; 
	  break; 
	  case 6:x="今天是星期六"; 
	  break; 
	  default:
	  x="期待周末";
	}

swich的比较是绝对比较，值和数据类型都会比较

switch后边的变量和case后边值的数据类型必须保持一致

必须带break；如果没有，条件成立后，后面的所以语句顺序执行并且不进行判断

    var a = "nihao";
    var b = new String("nihao");
	switch (a){ 
	  case b:
		x="=="; 
	  	break;  
	  default:
	  	x="===";
    }
    console.info(x);

## 3.JavaScript for 循环
语法

	for (语句 1; 语句 2; 语句 3) 
	{
	    被执行的代码块
	}
	语句 1 （代码块）开始前执行
	语句 2 定义运行循环（代码块）的条件
	语句 3 在循环（代码块）已被执行之后执行
例子

	cars=["BMW","Volvo","Saab","Ford"];

	for (var i=0;i<cars.length;i++){
		document.write(cars[i] + "<br>");
	}


### 3.1语句1
通常我们会使用语句 1 初始化循环中所用的变量 (var i=0)。

	for (var i=0,len=cars.length; i<len; i++)
	{ 
	    document.write(cars[i] + "<br>");
	}
	或者
	var i=2,len=cars.length;
	for (; i<len; i++){
		document.write(cars[i] + "<br>");
	}
### 3.2 语句2
通常语句 2 用于评估初始变量的条件。

如果您省略了语句 2，那么必须在循环内提供 break。

否则循环就无法停下来。这样有可能令浏览器崩溃。

	for (var i=0;;i++){
		document.write(cars[i] + "<br>");
		if(i>=cars.length-1){
            break;
        }
	}
### 3.3
通常语句 3 会增加初始变量的值。

语句 3 也可以省略（比如当循环内部有相应的代码时）：

    var i=0
	for (;;){
        document.write(cars[i] + "<br>");
		if(i>=cars.length-1){
            break;
        }
        i++;
	}

## 4. For/In 循环

	var person={fname:"John",lname:"Doe",age:25}; 
	 
	for (x in person)  // x 为属性名
	{
	    document.write(person[x] + "<br>");
	}
## 5.JavaScript while 循环 
### while 循环
语法

	while (条件) 
	{
	    需要执行的代码
	}
先判断条件，为真再执行代码

例子

    var i=0;
	while (i<5)
	{
	    document.write(i + "<br>");
	    i++;
	}
### do/while 循环
先执行一次，再进行循环

语法

	do
	{
	    需要执行的代码
	}
	while (条件);

例子

	do
	{
	    console.info("我就执行");
    }
    while (false)

## JavaScript Break 和 Continue 语句

break 语句可用于跳出循环

continue 语句跳出循环后，会继续执行该循环之后的代码（如果有的话）

### JavaScript 标签
如需标记 JavaScript 语句，请在语句之前加上冒号：

	label:
	statements

continue 语句（带有或不带标签引用）只能用在循环中

break 语句（不带标签引用），只能用在循环或 switch 中。

通过标签引用，break 语句可用于跳出任何 JavaScript 代码块：

	cars=["BMW","Volvo","Saab","Ford"];
	list: 
	{
	    document.write(cars[0] + "<br>"); 
	    document.write(cars[1] + "<br>"); 
	    document.write(cars[2] + "<br>"); 
	    break list;
	    document.write(cars[3] + "<br>"); 
	    document.write(cars[4] + "<br>"); 
	    document.write(cars[5] + "<br>"); 
	}

[https://www.runoob.com/js/js-type-conversion.html](https://www.runoob.com/js/js-type-conversion.html)