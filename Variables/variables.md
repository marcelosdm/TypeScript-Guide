# Typescript Variables

Here we see how to "type" variables in Typescript.

There are four different ways to declare a variable, and also four different data types. 
First, let's see those ways to declare:

1 - Declare the variable name, followed by the type:
	let name: string;

2 - Delare the variable name and don't specify the type, but it is inferred, and set its value:
	let name = 'Lebron James';

3 - Declare the variable name, specify the type and set its value:
	let name:string = 'Lebron James';

4 - Declare only the variable name. This will make its data type be set to "any", by default.
	let name;

Now, let's take a look on the different data types:

1 - let isStater: boolean

2 - let points: number

3 - let name: string

4 - let name: any

The type "any", can be set manually or by default (like we saw before).
If a variable is set to the type "any", it will work exactly as a JavaScript variable, that is, when it has a value of another type assigned to it later, the compiler won't be able to detect a problem.

