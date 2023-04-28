  # What's Typescript?

  it's a language that is built on top of JavaScript.

  ## Benefits of Typescript?

  - Static typing 
  - Code completion
  - Refactoring
  - Shorthand notations

  ## Drawbacks of Typescript ?

  - Compilation Time (it will be converted to JavaScript first)

  ## Types of Typescript ?

  - **any**: used when value could be any (not recommended to use, it's best to always define the exact type to avoid crashes).
  - **unknown**: used when type is unknown, like third party library with values of unknown types. other examples are JSON objects or writing apis that accept inputs of unknown type.
  - **never**: used when writing a function that always throws an error, or function that won't return anything, or functions with infinite loops.
  - **tuples**: used for fixed length array of different types of data.
  - **enums**: used for fixed constant values.

  ## How do we compile a Typescript file ?

  We use tsc filename.any

  ## How do we configure Typescript ?

  We use <pre><code>``` tsc --init ```</code></pre> to create a config file

  ## How do we debug Typescript files ?

  In vscode, we could click on the debugging option to create a launch.json file
  and then click on the line we want to debug so the compiler knows which line
  needs to be debugged.

  ## enum Best practices ?

  We could use const before defining the enum to make the compiler generate more optimized code.

## Typescript Fundamentals

### arrays

``` const nums: number[] = [] ```

By using this syntax, we are declaring that the values of this array are and will be numbers only.



### Tuples

Tuples are basically fixed length array values of different types. for example: 

```  const user: [string, number] = ['Rami', 45]```



### Enums

**enum** is used whenever we want to declare a set of constant values. for example, a set of different clothes sizes:

``` const enum  Size = {small, medium , large}```

#### why did we use const?

to generate more optimized code when it's compiled into JavaScript.

#### why did we use Pascal case to name it?

it's a best practice to use Pascal case when we declare types, enums, or interfaces in typescript.

#### what's the values of the Size here?

the values will start at 0 (small = 0). But, we could change that by setting small to 1``` small = 1 ```. this will make the values start from 1, which means medium is 2, and large is 3.



### Functions

When we declare a function in Typescript, we always have to set the type of the returned value, as well as declaring the types for any passed properties. For example: 

```
function sum(num1: number, num2: number): number{
	return num1 + num2
}
```

if we remove the ```:number``` after the parentheses,  the return value will be dynamically set to anything we return, so if we for example return a string ``` return 'rami'```. The value of the sum function will be a string as well. This could create bugs in our application later, so we should always remember to declare function's values.

if our function is not expected to return anything, we could use ```void``` type annotation. 

```
function sum(): void {
	// etc...
}
```



