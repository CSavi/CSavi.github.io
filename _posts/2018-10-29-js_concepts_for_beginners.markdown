---
layout: post
title:      "JS Concepts for Beginners:"
date:       2018-10-29 16:24:37 +0000
permalink:  js_concepts_for_beginners
---


**What is *context*?**

Context is always the value of the *this* keyword, which references the **object** that “owns” the currently executing code. Every function invocation has both scope and context. Scope is function-based, whereas, context is object-based. This means scope pertains to the variable access of a function when invoked and context is always the value of the *this* keyword.

If in a standalone function, *this* defaults to a global object or undefined. If located inside an object method, *this* refers to the object receiving the method call. If located outside any function, *this* always refers to the global object.


**What is *scope*?**

Scope is the context in which a variable exists –where the variable can be accessed and whether you have access to the variable in that context. A variable’s scope can be considered as local or global in JavaScript. 

Local variables (function-level scope) are variables declared within a function and are only accessible within that function or by its nested/inner functions. Also, local variables have priority over global variables within functions. If you declare a local and global variable with the same name, the local variable will have priority when you use it inside the function (local scope). 

Global variables are always declared outside the function or if they are initialized (assigned a value) and declared with the *var* keyword inside the function. This global context is considered the window object (HTML document) and can be accessible from anywhere in your code. 


**Demo of Function-Level Scope**


```
var name = “Ashley”;

function showName() {
	let name = “Mark”;  	// local variable; only accessible in showName()
	console.log(name);  	// Mark
}
console.log(name); 	// Ashley; global scope 

```



**What is *hoisting*?**

If using *var* to declare your variables, those declarations are automatically hoisted, or moved to the top of current referenced scope. *Const* and *let* must be declared at the beginning of a block as they are not automatically hoisted. Functions that use function declarations are also automatically hoisted, but not the assignment part of their expressions.

```
(function() {
var hero; 	// declarations are hoisted but NOT assignment
var antiHero;

	console.log(hero);	// undefined
	var hero = “Spiderman”;  	
	antiHero();		// TypeError: antiHero is not a function
let antiHero = function() {
console.log(“The Vulture”);
	}
});

```


**ES6 implications?**

With ES6, ***let*** and ***const*** were created. *Let* allows you to reassign a value, whereas *const* prevents you from reassigning. Rather than being scoped to the function, *let* and *const* are scoped to the block. A block is a set of opening and closing curly brackets in a function. These keyword variable declarations will hoist the variable to the top of the block; however, it will throw a ReferenceError if referencing the variable in the block before variable declaration.  The difference between *var* function declarations and *let*/*const* declarations is in the initialization phase.  *Var* declarations are automatically hoisted. *Let* and *const* need to be declared at the beginning of a block because they are not automatically hoisted.


**Variable Declaration Keywords: *var* vs *let***


```
var hero = “Spiderman”;
let antiHero = “Venom”;

if (true) {
	var hero = “Spider-Girl”;  	// global scope
	let antiHero = “The Vulture”;  	// local scope (block-level)
	console.log(hero);  		// “Spider-Girl”
	console.log(antiHero);  	// “The Vulture”
}
console.log(hero); 	// “Spider-Girl”
console.log(antiHero); 	// “Venom”


```



ES6 also brings **arrow functions**. They provide an abbreviated syntax to declare functions. Parentheses are optional for single parameters, but are required for multiple or no parameters.

(param1, param2, …, paramN) => { statements }
(param1, param2, …, paramN) => expression

(singleParam) => { statements } 
singleParam => { statements }

 () => { statements }


In addition, arrow functions lexically bind their context so *this* refers to the originating context. This creates lexical scoping, which simply means that it uses *this* from the code that contains the **arrow function**. These functions follow normal variable lookup rules. In other words, while searching for *this*, which is not present in current scope, they detect *this* from its enclosing scope.


```
// ES6
var obj = {
	id: 42,
	counter: function counter() {
		setTimeout(() => {
			console.log(this.id); 		// this === obj
}, 1000);
	}
};

```



