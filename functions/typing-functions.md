# Functions

## Intro

As said in the [TypeScript Documentation](https://help.github.com/articles/basic-writing-and-formatting-syntax/):
> Functions are the fundamental building block of any applications in JavaScript. They’re how you build up layers of abstraction, mimicking classes, information hiding, and modules. In TypeScript, while there are classes, namespaces, and modules, functions still play the key role in describing how to do things. TypeScript also adds some new capabilities to the standard JavaScript functions to make them easier to work with.

## Creating a function

As the reference above shows, here we'll see some new capabilities to the functions. We can add types to the parameters and even to the returns. See more bellow.

### Typing

Let's take a look on a basic **TypeScript** function. Here, we're typing the parameter, but as there's no return, its type is set to *void*:

```
function threePointPlay(player: string):void {
	console.log('Three point play by ' + player)
}
```

In the next example, we can see both the **parameter** and the **return** typed:

```
	let foulOut = function(foulsNum:number):boolean {
		return foulsNum > 5
}
```
In the **foulOut** function, we can see that if the arguments is set correctly, the function works:

```
console.log(foulOut(6));
> true
```

But if the arguments is not a *string*, for example, the compiler will throw an error:
```
console.log(foulOut("6"));
```




