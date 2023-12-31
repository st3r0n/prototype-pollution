# prototype-pollution
referesher about inheritance and prototype in java
JavaScript uses a prototypal inheritance model, 
which is quite different from the class-based model used by many other languages

eg of objects in javascript:
const user =  {                                                       
    username: "wiener",
    userId: 01234,
    isAdmin: false
}
or 
const user =  {
    username: "wiener",
    userId: 01234,
    exampleMethod: function(){
        // do something
    }
}

what is prototype:--->  prototypes are a blueprint or template for creating objects
The prototype object contains properties and methods that are shared by all instances of a particular object
Every object in JavaScript is linked to another object of some kind, known as its prototype
so prototype is also an object in which their default propertiesa re defined
getPrototypeOf()   ---. return prototype

in simple words protoype is just a template for any onject that has that same data type which contains 
predefined codes and methods which can be inherited and used by objects taht inherit them
Whenever you reference a property of an object, the JavaScript engine first tries to access this directly on the object itself. 
If the object doesn't have a matching property, the JavaScript engine looks for it on the object's prototype instead. 

![image1](https://portswigger.net/web-security/prototype-pollution/images/prototype-pollution-inheritance.svg)

prototype chain

Note that an object's prototype is just another object, which should also have its own prototype, and so on. 
As virtually everything in JavaScript is an object under the hood, this chain ultimately leads back to the top-level Object.prototype, 
whose prototype is simply null

++++++++++++++ACCESSING PROTOTYPES+++++++++++++++++++++
use __proto__  ---> to access its prototype

we can chain multiple __proto__ to access root proto
eg --> username.__proto__                        // String.prototype
username.__proto__.__proto__              // Object.prototype
username.__proto__.__proto__.__proto__    // null


