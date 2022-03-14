# Javascript-Topics

### Event bubbling and Event capturing

### Debounce and Throttle

### Prototype and Prototype chaining

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
