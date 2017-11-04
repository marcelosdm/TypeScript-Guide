# Arrays

In Typescript, there are three different ways to declar arrays:

1. Declaring its **type** followed by **brackets**.

	```typescript 
	let players:number[] = [23, 9, 0];
	```

2. Declaring the **Array class**, assigned to the **type**.

	```typescript
	let players:Array<number> = [23, 9, 0];
	```

3. Declaring **just the variable** with its **values between the brackets**. This way, its **type will be inferred**.
	
	```typescript
	let players = [23, 9, 0];
	```
