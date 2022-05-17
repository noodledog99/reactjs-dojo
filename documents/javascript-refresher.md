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
- Use <mark>const</mark>  if you plan on creating a [<span style="color:white">constant</span>](## "con·stant (noun): ค่าคงตัว, ค่าคงที่") value, so something which you only assign once and never change.