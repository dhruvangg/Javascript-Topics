### 

```
const a = [1]
const b = 2
b.push(2)
console.log(a, b);
```
> b.push is not a function (b is number)

2.  ```
    const obj = {
        a: this,                    //  will return window object
        b: function(){              //  will return obj
            return this;    
        },
        c: () => {                  //  will return window object
            return this;
        },
        d(){                        //  will return obj
            return this;
        },
        e: function(){              //  will return window object
            return this.a;
        }
    }
    ```
### Macro, Micro tasks, event loop, stack

```
console.log(1)
setTimeout(() => {
    console.log(2)
},0)
Promise.resolve().then(() => console.log(3))
setTimeout(() => {
    console.log(4)
}, 1)
console.log(5)


```
### Following code return an error
```
const Author = {
    name: "Dhruvang Gajjar",
    post: Post
}

const Post = {
    name: "Hello World", 
    author: Author
}
```
To resolve the error, we can use the following code of Hoisting:
```
const Author = {
    name: "Dhruvang Gajjar",
    post: function(){
        return Post
    }
}

const Post = {
    name: "Hello World", 
    author: function(){
        return Author
    }
}
```
# Get random number from a given range

```
function getRandom(max, min){
    return Math.floor(Math.random() * (max - min) + min)
}
```


