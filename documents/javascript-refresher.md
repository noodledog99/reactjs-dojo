<link href="../style.css" rel="stylesheet"></link>

# JavaScript Refresher

## Understanding **let**, **const** & **var**

### **<mark class="header">Var</mark>**

<mark>var</mark> is function scoped when it is [<span style="color:white">declared</span>](## "de·clar (verb): ประกาศ") [<span style="color:white">within</span>](## "with·in (noun): ภายใน, ข้างใน") a function. This means that it is [<span style="color:white">available</span>](## "a·vail·a·ble (adjective): สามารถใช้ได้") and can be accessed only within that function

- <mark>var</mark> variables can be re-declared and updated
- <mark>var</mark> variables are hoisted to the top of their scope and initialized with a value of <mark>undefined</mark>

<hr/>

### **<mark class="header">Let</mark>**

### **let is block scoped.**

> A block is a chunk of code bounded by {}. A block lives in curly braces. Anything within curly braces is a block.

So a variable declared in a block with <mark>let</mark> is only available for use within that block.

### **let can be updated but not re-declared.**

Just like <mark>var</mark>, a variable declared with <mark>let</mark> can be updated within its scope. Unlike <mark>var</mark>, a <mark>let</mark> variable cannot be re-declared within its scope.

### **Hoisting of let**

Just like <mark>var</mark>, <mark>let</mark> [<span style="color:white">declarations</span>](## "dec·la·ra·tion (plural noun): ประกาศ") are [<span style="color:white">hoisted</span>](## "/hoist/ (verb): ยก") to the top. Unlike <mark>var</mark> which is [<span style="color:white">initialized</span>](## "in·i·tial·ize (verb): เริ่มต้น") as <mark>undefined</mark>, the <mark>let</mark> keyword is not initialized. So if you try to use a let variable before declaration, you'll get a Reference Error.

<hr/>

### **<mark class="header">Const</mark>**

Variables declared with the <mark>const</mark> maintain [<span style="color:white">constant</span>](## "con·stant (noun): ค่าคงตัว, ค่าคงที่") values. <mark>const</mark> declarations share some similarities with <mark>let</mark> declarations.

### **const declarations are block scoped**

Like <mark>let</mark> declarations, <mark>const</mark> declarations can only be accessed within the block they were declared.

### **const cannot be updated or re-declared**

This means that the value of a variable declared with <mark>const</mark> remains the same within its scope. It cannot be updated or re-declared.

### **Hoisting of const**

Just like <mark>let</mark>, <mark>const</mark> declarations are hoisted to the top but are not initialized.

So just in case the differnt:

- <mark>var</mark> declarations are globally scoped or function scoped while <mark>let</mark> and <mark>const</mark> are block scoped.
- <mark>var</mark> variables can be updated and re-declared within its scope; <mark>let</mark> variables can be updated but not re-declared; <mark>const</mark> variables can neither be updated nor re-declared.
- They are all hoisted to the top of their scope. But while <mark>var</mark> variables are initialized with <mark>undefined</mark>, <mark>let</mark> and <mark>const</mark> variables are not initialized.
- While <mark>var</mark> and <mark>let</mark> can be declared without being initialized, <mark>const</mark> must be initialized during declaration.
- Use <mark>let</mark> if you want to create a variable that really is variable.
- Use <mark>const</mark> if you plan on creating a [<span style="color:white">constant</span>](## "con·stant (noun): ค่าคงตัว, ค่าคงที่") value, so something which you only assign once and never change.

<br/>

## Arrow Functions

### <mark class="header">this</mark> Keyword

<mark>this</mark> keyword is one of the most used keywords in JavaScript. But when it comes to regular functions and arrow functions, it behaves in entirely different ways.

<pre>
In regular function, <mark>this</mark> changes according to the way that function is invoked  
Simple Invocation
</pre>

- Simple Invocation: <mark>this</mark> equals the global object or maybe undefined if you are using strict mode.
- Method Invocation: <mark>this</mark> equals the object that owns the method.
- Indirect Invocation: <mark>this</mark> equals the first argument.
- Constructor Invocation: <mark>this</mark> equals the newly created instance

<pre>
<mark>Simple Invocation</mark>
function simpleInvocation() {
  console.log(this);
}
simpleInvocatoin(); // logs global object
--------------------------------------------------------------------
<mark>Method Invocation</mark> 
const methodInvocation = {
  method() {
    console.log(this);
  }
};
methodInvocation.method(); // logs methodInvocation object
--------------------------------------------------------------------
<mark>Indirect Invocation</mark>
const context = { value1: 'A', value2: 'B' };
function indirectInvocation() {
  console.log(this);
}
indirectInvocation.call(context);  // logs { value1: 'A' }
indirectInvocation.apply(context); // logs { value1: 'A' }
--------------------------------------------------------------------
<mark>Constructor Invocation</mark>
function constructorInvocation() {
  console.log(this);
}
new constructorInvocation(); // logs an instance of constructorInvocation
</pre>

But, in the <mark>arrow functions</mark>, the behavior of this changes completely.

<pre>
Arrow functions don't have their own <mark>this</mark>, and they don’t redefine the value of <mark>this</mark> within the function.
</pre>

Regardless of how you execute <mark>arrow functions</mark>, this inside an <mark>arrow function</mark> always refers to this from the outer context. This means that this keyword is lexically bound in <mark>arrow functions</mark>.

To understand it better, let’s consider the above example of Method Invocation with an arrow function to see the difference:

<pre>
var variable = "Global Level Variable";
let myObject = { 
    variable: "Object Level Variable", 
    arrowFunction:() => { 
        console.log(this.variable); 
    },
    regularFunction(){ 
        console.log(this.variable); 
    } 
};
myObject.arrowFunction(); 
myObject.regularFunction();

result:
"Global Level Variable" // because <mark>var</mark> is Global Variable
"Object Level Variable"
</pre>

This behavior of arrow functions makes them really useful when using callbacks inside methods.

You don't need to use workarounds like const self = <mark>this</mark> or callback.bind(<mark>this</mark>) with arrow functions, and it prevents any mistakes that can be caused by the use of <mark>this</mark> within callbacks.

<hr/>

## <mark class="header">Arguments Object.</mark>

In regular JavaScript functions, arguments keywords can be used to access the passed arguments when the function is invoked.

For example, If I call a function with 3 arguments, I will be able to access them using arguments keyword like this:

<pre>
function exampleFunction() {
  console.log(arguments[0]);
  console.log(arguments[1]);
  console.log(arguments[2]);
}
exampleFunction(1,2,3)

result:
1
2
3
</pre>

But, arrow functions <mark>do not have their own arguments</mark> and it uses the arguments from the outer function.

<pre>
let exampleFunction = {
 printArguments : () => {
  console.log(arguments);
 }
}
exampleFunction.printArguments(1,2,3)

result:
Uncaught ReferenceError: argument is not definded
</pre>

However, if you want to access arguments directly in an arrow function, you can use the <mark>rest parameters</mark> feature:

<pre>
let exampleFunction = {
 printArguments : (…args) => {
 console.log(…args);
 }
}
exampleFunction.printArguments(1,2,3);

result: 
1 2 3
</pre>

<hr/>

## <mark class="header">Constructors / **new** keyword</mark>

As well know, we can easily construct objects with regular functions. We just need to invoke the function with the <mark>new</mark> keyword.

<pre>
function Article(topic) {
  this.topic= topic;
}

const article = new Article('JavaScript');
</pre>

However, arrow functions <mark>can not be used as constructors</mark>.

<hr/>

## <mark class="header">Implicit return</mark>

In regular functions, we can use the <mark>return</mark> keyword to return any value from a function. If we don’t return anything, the function will implicitly return <mark>undefined</mark>.

<pre>
function exampleFunction() {
 return 10;
}
exampleFunction(); // output -> 10
--------------------------------------------------------------------
function exampleFunction() {
 var number  = 10;
}
exampleFunction(); // output -> undefined
--------------------------------------------------------------------
function exampleFunction() {
 var number  = 10;
  return;
}
exampleFunction(); // output -> undefined
</pre>

Arrow functions behave in the same way when returning values. But there is one [<span style="color:white">advantage</span>](## "ad·van·tage : ข้อได้เปรียบ") you can take from it.

<pre>
const addOne = (number) => number + 1;
addOne(10);

result: 11
</pre>

you might feel that arrow functions are better than regular functions. But, that’s not true for all cases, and there are some situations you should avoid using arrow functions.

> It is recommended to use regular functions when dealing with Promises, Callback functions with dynamic context, and Object methods.