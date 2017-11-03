# Classes

## Intro

> Traditional JavaScript uses functions and prototype-based inheritance to build up reusable components, but this may feel a bit awkward to programmers more comfortable with an object-oriented approach, where classes inherit functionality and objects are built from these classes. Starting with ECMAScript 2015, also known as ECMAScript 6, JavaScript programmers will be able to build their applications using this object-oriented class-based approach. In TypeScript, we allow developers to use these techniques now, and compile them down to JavaScript that works across all major browsers and platforms, without having to wait for the next version of JavaScript.

[TypeScript Documentation](http://www.typescriptlang.org/docs/handbook/classes.html)

In other words, we can say that a **Class** is the definition of an object. Classes contain the **attributes** *(characteristics)* of the object.

For example, we can create a house class . Then we can construct houses based on this class. It's as if the class were a model and it's characteristics were: *"open the window"*, *"turn on the light"*.

We can even use this class to create more complex houses, but **extending** the same class, without rewriting the same code again.

An **object** is an instance of the class. That is, we can create as many objects as we need.

## Defining a Class

Classes are created by using the key word *class*, followed by the class name. The convention for it, is to use the UpperCamelCase.

Basically, the class can have:
- **properties/attributes**;
- **constructor**;
- **methods**. 

In this case, the property *language* is a public property, by default. That means, other objects can access and change its value.
The **constructor**, is used to initialize the objects created in this class. 
You can see that when we refer to one object of the class we prepend *this*.

See the example bellow. Our class has three members:

- a property called **language**;
- a **constructor**;
- a method called **message**.

```typescript
class ProgrammingLanguage {
    
        language: string;
        
        constructor (message: string) {
            this.language = message;
        }
        
        message() {
            // return 'I love ' + this.language;
            console.log('I love ' + this.language);
        }
    }

```



