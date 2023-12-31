"On two occasions I have been asked, 'Pray, Mr. Babbage, if you put into the machine 
wrong figures, will the right answers come out?'[...] I am not able rightly to 
apprehent the kind of confusion of ideas that could provoke such a question."
--Charles Babbage, *Passages from the Life of a Philosopher* (1864)

### Arrays
The first index of an array is zero, not one. Zero-based counting has a long tradition
in technology and in certain ways it makes a lot of sense, but it takes some getting 
used to. Think of the index as the amount of items to skip, counting from the start of 
the array.


### Properties
The two main ways to access properties in JS are with a dot and with square brackets.
Bothe `value.x` and `value[x]` access a property on `value`, but not necessarily the 
same property. The difference is in how `x` is interpreted. 

- When using a dot, the word after the dot is the literal name of the property.
- When using square brackets, the expression between the brackets is evaluated to get
the property name.

Wheras `value.x` fetches the property of `value` named `x`, `value[x]` tries to evaluate
the expression `x` and uses the result, converted to a string, as the property name.

If you know that the property you are interested in is called _color_, you say 
`value.color`. If you want to extract the property named by the value held in the 
binding _i_, you say `value[i]`.


### Methods
A stack, in programming, is a data structure that allows us to push values into
it and pop them out again in the opposite order so that the thing that was added
last is removed first.


### Array Loops
A loop like this:
```js
for (let = i 0; i < JOURNAL.length; i++) {
  let entry = JOURNAL[i]
  // Do something with entry
}
```
is very common in classical JS, going over arrays one element at a time is 
something that comes up a lot, and to do that you'd run a counter over the length
of the array and pick  out each element in turn.

There is a simpler way to write such loops in modern JS.
```js
for (let entry of JOURNAL) {
  // Do something with entry
}
```
When a `for` loop looks like this, with the word `of` after a variable definition,
it will loop over the elements of the value given after `of`. This works not only 
for arrays but also for strings and some other data structures.
