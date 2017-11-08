# Namespaces
## Intro

>As we alluded in our note about terminology, “internal modules” are now referred to as “namespaces”. Additionally, anywhere the module keyword was used when declaring an internal module, the namespace keyword can and should be used instead. This avoids confusing new users by overloading them with similarly named terms.
[TypeScript Documentation](http://www.typescriptlang.org/docs/handbook/namespaces.html)

So, we can say that we use **namespaces** when we want to organize the code avoiding name conflicts.



## Namespacing

### Exporting an object

As with the modules, only what's exported is available to be used externally.
Take a look at the example:

```typescript
namespace Utilities {

	export class PlayerStats {...}

	function threePointPlay (...) {...}
}
```

Note that just the *class* **PlayerStats** is exported here.

### Using the exported

To use the exported object, see that the syntax is made declaring ***///*** followed by the key words **reference path** and the file name. Note that this time, we need to use the file extension.

```typescript
/// <reference path = "Utilities.ts" />
```

## What not to do

It's common to see developers exporting the whole namespace. But watch out! This will make the namespace useless. So, don't treat your namespace like a module.
