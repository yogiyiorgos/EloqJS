"An abstract data type is realized by writing a special kind of program [...]
which defined the type in terms of the operations which can be performed on it"
--Barbara Liskov, *Programming with Abstract Data Types*

In programming culture, we have a thing called *object-oriented programming*, a
set techniques that uses objects and related concepts as the central principle
of program organization.

### Encapsulation
The core idea in object-oriented programming is to divide programs into smaller 
pieces and make each piece responsible for managing its own state.

This way, some knowledge about the way a piece of the program works can be kept
*local* to that piece. 

Different pieces of such a program interact with each other through *interfaces*,
limited sets of functions or bindings that provide useful functionality at a more
abstract level, hiding their precise implementation.

Such program pieces are modeled using objects. Their interface consists of a 
specific set of methods and properties. Properties that are part of the interface 
are called public. The others, which outside code should not be touching, are 
called private.


### Classes
A class defines the shape of a type of object - what methods and properties it has.
Such an object is called an *instance* of the class.

To create an instance of a given class, we have to make an object that derives
from the proper prototype, but we also have to make sure it, itself, has the
properties that instances of this class are supposed to have. This is what a 
*constructor* function does.

```js
function makeRabbit(type) {
  let rabbit = Object.create(protoRabbit)
  rabbit.type = type
  return rabbit
}
```

Constructors, all functions in fact, automatically get a proprty named `prototype`,
which by default holds a plain, empty object that derives from `Object.prototype`.
By convention, the names of constructors are capitalized os that they can easily be
distinguished from other functions.

