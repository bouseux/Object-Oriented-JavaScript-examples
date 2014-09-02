Object-Oriented-JavaScript-examples
===================================

Tutorial which I took to sharpen up my Javascript skills.
Tutorial from TutsPlus at https://code.tutsplus.com/courses/object-oriented-javascript/lessons/introduction .

Some things that I learnt:
 - You can only self-invoke functions that were built using function expression. For example,
 `var foo = function() {}();`
 - The reason you need parentheses around self-invoking anonymous functions is because the Javascript parser otherwise interprets it as function declaration which cannot be self-invoked. Thus it has to look like this '(function() {}());'
 - Instead of surrounding self-invoking anonymous functions with (), you can just append tenary operator in the beggining such as '+function() {}();' so that the Javascript parser knows it's not a function declaration.
 - A benefit of using IIFE’s ( Immediately Invoked Function Expression ) is the ability to pass global objects (window, document, jQuery) to an anonymous function, and reference global objects within the function's scope.
 - Since anonymous function is not assigned to a global variable, no global property is being created, and all of the properties created inside of the function expression are scoped locally to the expression. This leaves the global namespace cleaner.
 - 
