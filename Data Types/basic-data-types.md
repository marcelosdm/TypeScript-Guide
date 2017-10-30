# TypeScript Basic Data Types

As written in the [TypeScript documentation](https://www.typescriptlang.org/docs/handbook/basic-types.html):

> For programs to be useful, we need to be able to work with some of the simplest units of data: numbers, strings, structures, boolean values, and the like. In TypeScript, we support much the same types as you would expect in JavaScript, with a convenient enumeration type thrown in to help things along.

So, let's take a look on those different *basic* data types:

1. ```let isStater: boolean```

2. ```let points: number```

3. ```let name: string```

4. ```let name: any```

The type *"any"*, can be set manually or by default.
If a variable is set to the type *"any"*, it will work exactly as a **JavaScript** variable, that is, when it has a value of another type assigned to it later, the compiler **won't be able to detect a problem**.

