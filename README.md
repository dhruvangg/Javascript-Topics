# Javascript-Topics

### Primitive Types

In JavaScript, a primitive is data that is not an object and has no methods. There are 7 primitive data types: string, number, bigint, boolean, undefined, symbol, and null.
All primitives are immutable, i.e., they cannot be altered.

Now one question prompted in my mind that we can change any variable's value then How it can be immutable? So Here is the answer: 

```
let name = "Champ Decay"

name = "Dhruvang Gajjar"

name[0] = "A" // This will not change variable name

```

When you change the value of any variable, you're reassigning the value of varible not altering/mutating it

### Event bubbling

The bubbling principle is simple. When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.
In the event bubbling, The event is first captured and handled by the innermost element and then propagated to outer elements.

```
<form onclick="alert('form')">FORM
  <div onclick="alert('div')">DIV
    <p onclick="alert('p')">P</p>
  </div>
</form>
```

> For instance, a `focus` event does not bubble.

### Event Capturing

In the event capturing, The event is first captured by the outermost element and propagated to the inner elements.

> the capturing phase is rarely used. Normally it is invisible to us.

### Debounce and Throttle

The debounce() function forces a function to wait a certain amount of time before running again. The function is built to limit the number of times a function is called. 

```
function debounce(fun, timeout = 300) {
    let timer
    return (...args) => {
        clearTimeout(timer)
        timer = setTimeout(() => {
            fun.apply(this, args)
        }, timeout)
    }
}

elem.addEventListener('click', debounce(() => {
    console.log('Hello')
}))
```

The throttle() function is used to call a function after every millisecond or a particular interval of time only the first click is executed immediately.

```
function throttle(fun, timeout = 300) {
    let timer
    return (...args) => {
        if (!timer) {
            timer = setTimeout(() => {
                fun.apply(this, args)
                timer = null
            }, timeout)
        }
    }
}

elem.addEventListener('click', throttle(() => {
    console.log('Hello')
}))
```

### Prototype and Prototype chaining

### Shadowing

### Temporal dead zone

### Call by Value and Call by Reference

### Closure

### Call, Apply and Bind

### Constructor

The constructor method is a special method of a class for creating and initializing an object instance of that class.

A constructor enables you to provide any custom initialization that must be done before any other methods can be called.

If you don't provide your own constructor, then a default constructor will be supplied for you. If your class is a base class, the default constructor is empty:
> constructor() {}

### OOP Concepts of JavaScript

### Automatic Semicolon Insertion (ASI)

Unlike other C-like languages, JavaScript does not enforce the use of a semicolon at the end of a statement. Instead, the semicolon is optional, and the JavaScript interpreter will "intelligently" add them when it runs the code.

In JavaScript, a semicolon is automatically inserted when,
- two statements are separated by a line terminator
- two statements are separated by a closing brace ('}')
- a line terminator follows a break, continue, return, or throw.

| Entered code | "Understood" as | Corrected code | 
|--|--|--|
| return <br/> 2a + 1;|return; <br/> 2a + 1; | return 2a + 1; |
| i<br/>++; | i;<br/>++; | i++; |
