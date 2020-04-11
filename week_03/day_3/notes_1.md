### Week 3 - Day 3

#### Session 1


## `Functions`:

You would have seen functions before but now you can also write your own functions!

### Example:

```javascript
function square(number) {
  return number * number;
}
```

The `function` keyword defines the start of a function. Functions also have a name, the above function's name is `square`.  
Functions are used to represent `blocks` of code that perform very specific functions. Just like `if` statements all the code within the braces `{}` are executed by the function. 

Executing a function is called invoking, calling, or applying it.  You can call a function by putting parentheses after an expression that produces a function value. 

Functions also have `arguments`,  these are values you can pass to a function. In the example `number` is the argument we are passing to the function.

Functions also have a `return` statement, they are optional but many functions `return` some data that can be used later in your overall program. 

[https://codepen.io/albseb511/pen/jOOzbog](https://codepen.io/albseb511/pen/jOOzbog)

### `While Loops`

Lets say we wanted to run a piece of code multiple times. We could write out duplicate code multiple times but loops save us a lot of time and make our code efficient!

For example, let’s say we wanted to print "Hello World!" 100 times. It would be impractical to write `console.log("Hello World!")` 100 times. 

This is where loops are useful.

Example:

```javascript 

var i = 0

while(i < 100){
	console.log("Hello World!")
	i++
}

```

The above code prints ```Hello World!``` 100 times, try it out for yourself!

*How does it work?* 

The loop in the code is called a while loop. It can execute a block of code as long as a specified condition is ```true```. 

In the above example the while loop prints ```Hello World!``` until ```i == 100```.

Notice the line ```i++```. This is another simpler way of doing ``` i = i + 1 ```. You can also do ```i--``` which is a simpler way of doing ```i = i - 1 ```.

Once i is equal to 100 the loop **breaks** and stops executing the code within. 

Here's another example:

```javascript
var i = 0
while(true){
	console.log(i)
	i++
}
console.log("This line of code will never execute")
```

The above loop is called an infinite loop since the specified condition is always ```true```. The loop will run forever which is often undesirable since we want to break out of loops to do other useful work in our program.  
**Note:** Please do not try to run a infinite loop on your browser as this can cause your browser to crash. If you run and infinite loop and your browser freezes all you can do is try and close it!  

### How do we fix this?

By using a ```break``` statement. 

Example:

```javascript
var i = 0
while(true){
	console.log(i)
	if(i == 100){
		break
	}
	i++
}
console.log("This line of code will execute after i equals 100")
```

Now our loop will gracefully break after i equals 100 and the next line of code which prints ```"This line of code will execute after i equals 100"``` will be executed. 

### `For loops`

The next kind of loop in JavaScript is a for loop. 

Example:

```javascript 
for(var i = 0; i < 100; i++){
	console.log("Hello World!")
}
```

This again prints ```Hello World!``` 100 times. For loops work in much the same way as while loops.

`i < 100` represents the limit condition, after which the loop stops executing. 


### `break` vs `continue`:

using break exits the loop and continue with rest of the program

using continue will exit and not execute any code after it, but will go back to the loop

[https://codepen.io/albseb511/pen/gOOerEm](https://codepen.io/albseb511/pen/gOOerEm)

### More Strings!

We can get the length of any `string` by using the `.length` property of a string.

**Example:**
```javascript
var s = "Masai School!"
console.log(s.length)
```

**Output:**
```javascript
13
```

We can access any element of a string by using its index.

**Example:**

```javascript
var s = "Masai School"
var e1 = s[0]
var e2 = s[3]
var e3 = s[s.length-1]
console.log(e1)
console.log(e2)
console.log(e3)
```

**Output:**
```javascript
M
a
l
```

In the above code `s[0]` accesses the first character of the string `s` and `s[s.length-1]` accesses the last element of the string `s`.

If you are wondering why the first element is not `s[1]` this is because of **Zero-based Indexing**. You can read more about it here [http://www.cs.utexas.edu/users/EWD/transcriptions/EWD08xx/EWD831.html](http://www.cs.utexas.edu/users/EWD/transcriptions/EWD08xx/EWD831.html)

Lastly you can also use loops to access every character in a string one-by-one. 

**Example:**

```javascript
var s = "Masai School is amazing!"

for(var i = 0; i < s.length; i++){
	console.log(s[i]);
}
```

**Output:**

```javascript
M
a
s
a
i

S
c
h
o
o
l

i
s

a
m
a
z
i
n
g
!
```

[https://codepen.io/albseb511/pen/ExxENPe](https://codepen.io/albseb511/pen/ExxENPe)

## Scope

In programing **Scope** determines the accessibility (visibility) of variables.

There are two types of scope in JavaScript:

- Local Scope 
- Global Scope

### Local Variables

Consider the following snippet of code

```javascript
// code here cannot access the `number` variable!
function someFunction(){
    var number = 20
}
// code here cannot access the `number` variable!
```

In the above example only the code within the funciton `someFunction` can access the `number` variable. 

## Global Variables

Consider another snippet of code

```javascript
var number = 20
//code here can access the `number` variable!
function someFunction(){
    //code here can access the `number` variable!
}
//code here can access the `number` variable!
```

The variable `number` is said to be a global variable and can be accessed by any line of code below its declaration. 

## Local Scope within functions

Consider one last example

```javascript
function loop(){
	for(var i = 0; i < 10; i++){
		console.log(i)
	}
	// the variable `i` can be accessed here
}
// the variable `i` cannot be accessed here
```
In the above example since `i` is declared within the for loop it cannot be accessed outside it!


### Codepen with complex examples!

[https://codepen.io/albseb511/pen/QWWmGMM](https://codepen.io/albseb511/pen/QWWmGMM)



## keywords

Here are some keywords that javascript has. If you use this in declaring your variables or other names,
you will be given an error.

```
break case catch class const continue debugger default
delete do else enum export extends false finally for
function if implements import interface in instanceof let
new package private protected public return static super
switch this throw true try typeof var void while with yield
```


### Naming conventions for variables

```

    The first character must be a letter or an underscore (_). You can't use a number as the first character.

    The rest of the variable name can include any letter, any number, or the underscore. You can't use any other characters, including spaces, symbols, and punctuation marks.

    As with the rest of JavaScript, variable names are case sensitive. That is, a variable named Interest_Rate is treated as an entirely different variable than one named interest_rate.

    There's no limit to the length of the variable name.

    You can't use one of JavaScript's reserved words as a variable name. All programming languages have a supply of words that are used internally by the language and that can't be used for variable names because doing so would cause confusion (or worse). Note, too, that JavaScript also has many keywords that should be avoided as well.
```