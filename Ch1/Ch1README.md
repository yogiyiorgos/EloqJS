"Below the surface of the machine, the program
moves. Without effort, it expands and contracts.
In great harmony, electrons scatter and regroup.
The forms on the monitor are but ripples on the
water. The essense stays invisibly below."
--Master Yuan-Ma, *The Book of Programming*


### Empty Values
There are two special values written `null` and `undefinded`, that are used to 
denonte the absence of a *meaningful* value. They are themselves values, but 
they carry no information.
Many operations in the language that don't produce a meaningful value,
yield `undefined` simply because they have to yield some value.
The difference in meaning between `null` and `undefined` is an accident of 
JS's design and it doesn't matter most of the time. In cases where we actually 
need to concern ourselves with these values, it recommended to treat them 
mostly interchangably.
