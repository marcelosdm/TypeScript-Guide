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

    constructor (lang: string) {
        this.language = lang;
    }
    
    message() {
        console.log(`I love ${this.language}`);
    }
}


```

To create an object from this class, we use the key word **new** followed by the name of the class and passing the parameter. See bellow:

```typescript
    let programming = new ProgrammingLanguage('TypeScript');
```

Finally, to show the message in the console, we can call the method, like this:

```typescript
    programming.message();
```

### Making Things Easier

Another way to declare a class, is to put either the word *public*, or the word *private* before the constructor argument. Note that the property is now the constructor argument. You can even test the code by creating an object and calling the *message* method to see the result in the console, as we did above.

```typescript
    class ProgrammingLanguage {

    constructor (public language: string) {

    }
    
    message() {
        console.log(`I love ${this.language}`);
    }
}

```

## Inheritance

> In TypeScript, we can use common object-oriented patterns. Of course, one of the most fundamental patterns in class-based programming is being able to extend existing classes to create new ones using inheritance.
[TypeScript Documentation](http://www.typescriptlang.org/docs/handbook/classes.html)

See the example where we have the class *Player*. This class has the property *name* as an **argument**, and it's set as a **string** type. It also has a method called *game*, that has its **argument** called *pointsMade*, that is set as a **number** type, and already receives the **0** value. 
Imagine this class like being a model.

```typescript
class Player {

    constructor (public name: string) {}
    
    game(pointsMade: number = 0) {
        console.log(`${this.name} scored ${pointsMade} in the game.`)
    }
}

```

Now we've got a class called *Jordan*. This class **extends** the class **Player**. Think of it, as the class Jordan **inherits** all the basic features from the class Player. 
Here the constructor doesn't need to have any argument, because we're using the key word **super** to execute the constructor function on the base class (*class Player*). So, we're passing the name of the player directly here.
We also doing it in the *game* method, by using the **super** again.

In the end of this code, we also call the method *game*.

```typescript
class Jordan extends Player {

    constructor () {super('Micheal Jordan')}

    game(pointsMade = 40) {
        super.game(pointsMade);
    }
}

let jordan = new Jordan();
jordan.game();
```
