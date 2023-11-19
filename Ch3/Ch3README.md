"People think that computer science is the art of geniuses but the actual reality is the
opposite, just many people doing things that build on each other, like a wall of mini
stones."
--Donald Knuth

### Bindings and Scopes
Bindings declared with `let` and `const` are in fact local to the block they are
declared in, so when they are created inside of a loop, the code before and after
the loop cannnot "see" it. In pre-2015 JS, only functions created new scopes, so
old-style bindings, created with the `var` keyword, are visible throughout the 
whole function that they appear in-or throughout the global scope, if they are not
in a function.


### Nested Scope
The set of bindings visible inside a block is determinded by the place of that block
in the program text. Each local scope can also see all the local scopes that contain
it, and all scopes can see the global scope. This approach to binding visibility is 
called *lexical scoping*.


### Closure
The feature to be able to reference a specific instance of a local binding in an 
enclosing scope, is called closure. A function that references bindings from local
scopes around it is called a closure.

A good mental model to think of a function valuesd as containing both the code in
their body and the environment in which they are created. When called, the function body
sees the environment in which it was created, not the environment in which it was called.


### Recursion
A function that calls itself is called `recursive`.

```js
function power(base, exponent) {
  if (exponent === 0) {
    return 1
  } else {
    return base * power(base, exponent - 1)
  }
}
console.log(power(2, 3)) // -> 8
```
