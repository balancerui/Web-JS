1.js用法
	HTML中的脚本必须位于 <script> 与 </script> 标签之间。脚本可被放置在 HTML 页面的 <body> 和 <head> 部分中。
	引用外部的Js <script src="xx.js"></script>
2.js输出
	JavaScript 没有任何打印或者输出的函数。
	JavaScript 可以通过不同的方式来输出数据：
	（1）使用 window.alert() 弹出警告框。
	（2）使用 document.write() 方法将内容写到 HTML 文档中。
	（3）使用 innerHTML 写入到 HTML 元素。
	（4）使用 console.log() 写入到浏览器的控制台。
3.js函数
	function functionName() {
		函数体；
	}
	JavaScript是弱类型编程语言,定义变量都使用 var 定义,定义后可以通过 typeOf() 来获取JavaScript中变量的数据类型.
	
4.js语句
	js的语句是发给浏览器的命令。
	；封号用于分隔js语句
	在同一个代码块中的语句是一起执行的。
	JavaScript 是脚本语言。浏览器会在读取代码时，逐行地执行脚本代码。而对于传统编程来说，会在执行前对所有代码进行编译。
	
5.js变量
	一条语句中声明的多个不可以赋同一个值:
	var x,y,z=1;
	x,y 为 undefined， z 为 1。
	let变量:let var1 [= value1] [, var2 [= value2]] [, ..., varN [= valueN]];
	let允许你声明一个作用域被限制在块级中的变量、语句或者表达式。在Function中局部变量推荐使用let变量，避免变量名冲突。
	let 声明的变量只在其声明的块或子块中可用
6.js对象
	对象的属性之间一定要用逗号隔开;
	var person{name:"bob",age:18};
	var person {
		name:"bob",
		age:18
	};
	对象属性有2种寻址方式 ①person.name;	②person["name"];
	声明变量类型:当您声明新变量时，可以使用关键词 "new" 来声明其类型：
	var carname=new String;
	var x=      new Number;
	var y=      new Boolean;
	var cars=   new Array;
	var person= new Object;
	JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。
7.js对象
	①对象也可以是一个变量。
	var person={name:"bob",age:18};
	②对象属性：js对象是变量的容器，也是键值对的容器。
	③对象方法：定义了一个函数，并作为对象的属性存储。通过添加 () 调用 (作为一个函数)。
	④访问对象方法：
		（1）methodName : function() { code lines }
		（2）obj.方法名()
8.js函数
	function functionname()
	{
		执行代码
	}
	调用带参数的函数
	function myfunction(var1,var2)
	{
		变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值
	}
	
	即使不把它保存为变量，您也可以使用返回值：
	document.getElementById("demo").innerHTML=myFunction();
	在使用 return 语句时，函数会停止执行，并返回指定的值。例如：
	sayHi();
	function sayHi(name,message){
    document.write("return 语句执行前。");
    return;
    alert("hello" + name +"," + message);//这一行永远不会被调用
	}
9.js运算符
	var result1=5+5+"abc"; 		//结果将是"10abc"
	var result2= ""+5+5+"abc"; 	//结果将是"55abc"
10.js循环
	for (var i=0;i<cars.length;i++)
	{ 
		document.write(cars[i] + "<br>");
	}
	for-in:循环遍历对象的属性
11.typeOf属性
	检测变量的数据类型
	typeof "John"                // 返回 string 
	typeof 3.14                  // 返回 number
	typeof false                 // 返回 boolean
	typeof [1,2,3,4]             // 返回 object
	typeof {name:'John', age:34} // 返回 object
12.js数据类型 
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
	constructor 属性返回所有 JavaScript 变量的构造函数。
	typeOf和instanceOf的区别：
13.js错误
	try catch和throw
14.js表单
	HTML 表单验证可以通过 JavaScript 来完成。
	JavaScript实例：
		function validateForm() {
		var x = document.forms["myForm"]["fname"].value;
		if (x == null || x == "") {
			alert("需要输入名字。");
			return false;
			}
		}
	也可以用HTML表单实例来调用
	<form name="myForm" action="demo_form.php" onsubmit="return validateForm()" method="post">
	名字: <input type="text" name="fname">
	<input type="submit" value="提交">
	</form>
	HTML表单自动验证：
		如果表单字段 (fname) 的值为空, required 属性会阻止表单提交：
		<form action="demo_form.php" method="post">
			<input type="text" name="fname" required="required">
			<input type="submit" value="提交">
		</form>
	数据验证：
		数据验证用于确保用户输入的数据是有效的。
		典型的数据验证有：
			必需字段是否有输入?
			用户是否输入了合法的数据?
			在数字字段是否输入了文本?
		大多数情况下，数据验证用于确保用户正确输入数据。
		数据验证可以使用不同方法来定义，并通过多种方式来调用。
		服务端数据验证是在数据提交到服务器上后再验证。
		客户端数据验证 side validation是在数据发送到服务器前，在浏览器上完成验证。
