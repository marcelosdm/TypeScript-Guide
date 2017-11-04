# Typescript Variables

Here we'll see how to *"type"* variables in Typescript.

There are four different ways to **declare a variable**, and also four different **data types**. 
First, let's see those ways to **declare**.

1. Declare the **variable name**, followed by the **type**:

	```typescript
	let name: string;
	```

2. Delare the **variable name** and **don't specify the type** (but it is *inferred*) and set its **value**:

	```typescript
	let name = 'Lebron James';
	```

3. Declare the **variable name**, specify the **type** and set its **value**:

	```typescript
	let name:string = 'Lebron James';
	```

4. Declare **only the variable name**. This will make its data type be set to *__"any"__*, by default:

	```typescript
	let name;
	```

