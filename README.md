Object-Oriented-JavaScript-examples
===================================

Tutorial I took to sharpen up my Javascript skills.

Some things that I learnt:
 - You can only self-invoke functions that were built using function expression. For example,
 `var foo = function() {}();`
 - The reason you need parentheses around self-invoking anonymous functions is because the Javascript parser otherwise interprets it as function declaration which cannot be self-invoked. Thus it has to look like this `(function() {}());`
 - Instead of surrounding self-invoking anonymous functions with (), you can just append tenary operator in the beggining such as `+function() {}();` so that the Javascript parser knows it's not a function declaration.
 - A benefit of using IIFE’s ( Immediately Invoked Function Expression ) is the ability to pass global objects (window, document, jQuery) to an anonymous function, and reference global objects within the function's scope.
 - Since anonymous function is not assigned to a global variable, no global property is being created, and all of the properties created inside of the function expression are scoped locally to the expression. This leaves the global namespace cleaner.
 - It is faster to assign methods to object prototype rather than assigning method to each instantiated object in the constructor. This is a great performance boost since you are not redefining the method each time and all objects can still access the method.
 - If object's prototype does not have a method that was called, it goes up the chain and keeps looking until it reaches Object protype. The process of going up the chain is resources consuming.
 - In cases when you get very long chains such as `myObj.__proto__.__proto__.__proto__.toString();` which is not efficient, you can define myObj prototype like this `myObj.prototype = Object.create(Object.prototype);` so now there will be no chaining and toString() method is directly accessible, great win.
 - You cannot have private properties in Javascript. Those that you would like to be private, you can indicate using special notation, most common being appending two slashes at the front i.e. `__myPrivateProperty`.
 - The best practice is to start constructors with capital letter i.e. `var Person = function() {}`.

Tutorial from TutsPlus at https://code.tutsplus.com/courses/object-oriented-javascript/lessons/introduction .
