Text
====

Text-handling utility.

## `DEBUG`

Flag: Debug mode. (Default 1.)


## f

Interpolated string, emulating Python, e.g.

	      f'{2} plus {2} is {2+2}'
	2 plus 2 is 4
	      (A B)←2 3
	      f'{A} plus {B} is {A+B}'
	2 plus 3 is 5

An optional left argument is a ref to the context in which expressions are to be evaluated.
The default is the context in which `f` is called.

With Debug mode on, `f` signals errors in its argument; with it off, it silently returns its argument.

**Errors**

123: Nested or unbalanced braces, e.g. `'{foo'` or `'{{foo}}'`

