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
15.JS函数定义
	function functionName(a,b) {
		函数体/执行的代码
		return a*b;
	}
	分号是用来分隔可执行JavaScript语句。 
	由于函数声明不是一个可执行语句，所以不以分号结束。
函数表达式：
	var x = function(a,b){
		return a*b;
	}
构造函数function()
	var myFunction = new Function("a", "b", "return a * b");
	var x = myFunction(4, 3);
	函数可作为一个值使用
	function myfunction(a,b) {
		return a+b;
	}
	var x = myfunction(3,4);
	toString() 方法将函数作为一个字符串返回:
	function myFunction(a, b) {
		return a * b;
	}
	var txt = myFunction.toString();
16.JS函数参数
	JavaScript 函数定义时显式参数没有指定数据类型。
	JavaScript 函数对隐式参数没有进行类型检测。
	JavaScript 函数对隐式参数的个数没有进行检测。
	function myfunction(x,y){
		y = y || 0;	}
	argument对象包含了函数需要调用的参数数组
17.JS函数调用
	①作为方法调用
		var object = {
			firstName:"bob",
			lastName:"jaskon",
			fullName:function() {
				return this.firstName + " " + this.lastName;
			};
			
		}
		object.fullName;
	②使用构造函数调用函数
	如果函数调用前使用了 new 关键字, 则是调用了构造函数。
	// 构造函数:
	function myFunction(arg1, arg2) {
		this.firstName = arg1;
		this.lastName  = arg2;
	}
	var x = new myFunction("John","Doe");
	x.firstName;                             // 返回 "John"
18.JS闭包
	var add = (function () {
		var counter = 0;
		return function () {return counter += 1;}
		})();
		function myFunction(){
		document.getElementById("demo").innerHTML = add();
	}
	闭包就是一个函数引用另一个函数的变量，因为变量被引用着所以不会被回收，因此可以用来封装一个私有变量。这是优点也是缺点，不必要的闭包只会增加内存消耗。
	或者说闭包就是子函数可以使用父函数的局部变量，还有父函数的参数。
19.JS HTML-DOM（文档对象模型）
	网页在进行加载时，浏览器会创建页面的DOM
	通过可编程的对象模型，JavaScript 获得了足够的能力来创建动态的 HTML。
	JavaScript 能够改变页面中的所有 HTML 元素
		（1）改变HTML的输出流
			Document.write(Date());
		（2）改变HTML的内容
			Document.getElementById("demo").innerHTML="新文本"；
		（3）改变HTML的属性
			<img id="image" src="a.jpg">
			Document.getElementById("image").src="cc.png";
	JavaScript 能够改变页面中的所有 HTML 属性		
	JavaScript 能够改变页面中的所有 CSS 样式
		（1）改变HTML样式
			Document.getElementById("demo").style.color="red";
			Document.getElementClassName("demo").style.fontsize="Larger";
	JavaScript 能够对页面中的所有事件做出反应
		（1）使用事件
			<button type="button" onclick="document.getElementById("demo").style.color="red" ">
		（2）对事件做出反应
			<h1 onClick="this.innerHTML='ok!' " >点击文本</h1>
	HTML事件属性
		document.getElementById("myBtn").onclick=function(){displayDate()};
		onload 和 onunload 事件会在用户进入或离开页面时被触发。onload 和 onunload 事件可用于处理 cookie。
			<body onload="checkCookies()">
		onchange 事件常结合对输入字段的验证来使用。当用户改变输入字段的内容时，会调用 upperCase() 函数。
			<input type="text" id="fname" onchange="upperCase()">
		onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。
	DOM事件监听（EventListener）
		document.getElementById("id").addEventListener("click",displayDate);---向指定元素添加句柄
		添加事件句柄
		Element.addEventListener("click",function(){alert("hello"); });
20.JS HTML DOM节点
	①创建新的DOM节点 appendChild()--加在新元素末尾
	②插入节点 insertBefore()---将新元素添加到开始位置
	③替换HTML元素 replaceChild() 
21.HTML DOM 集合
		var x = document.getElementsByTagName()方法返回HTML Collection对象
		获取对象的length
			var myCollection = document.getElementsByTagName("p");
			document.getElementById("demo").innerHTML = myCollection.length;
22.JavaScript对象
	对象拥有属性和方法
	访问对象的属性：
		ObjectName.propertyName
		var x = "hello world";
		var y = x.length;
	访问对象的方法：
		ObjectName.method();
		var message = "hello world";
		var x = message.toUppercase();
	创建JS对象
		person = new object();
		person.firstName="bob";
		person.age=50;
		person={firstname:"John",lastname:"Doe",age:50,eyecolor:"blue"};
	使用对象的构造器
		function person(firstname,lastname,age,eyecolor)
		{
			this.firstname=firstname;
			this.lastname=lastname;
			this.age=age;
			this.eyecolor=eyecolor;
		}
	创建JS的实例
		var person = new Person("John",50,"blue");
	把方法添加到对象中去
		function Person(firstName,lastName) {
			this.firstName=firstName;
			this.lastName=lastName;
			function changeName(name) {
				this.lastName=name;
			}			
		
		}
	JS for-in循环
		for(var in object){
			for...in 循环中的代码块将针对每个属性执行一次。
		}
		实例：
		var person = {firstName:"john",age:25}
		for (x in person) {
			txt = txt + person[x];
		}
	引入外部的JS文件
	<script src="xx.js" type="text/javaScript"></script>
23.javaScript数组
	1.创建数组
	var myCars=new Array("Saab","Volvo","BMW");
	2.创建新方法
	原型是JavaScript全局构造函数。它可以构建新Javascript对象的属性和方法。
	Array.prototype.myUcase=function(){
    for (i=0;i<this.length;i++){
        this[i]=this[i].toUpperCase();
    }
}
	
	
