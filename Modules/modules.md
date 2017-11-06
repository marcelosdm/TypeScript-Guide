# Modules

Module is an independent unit which can contain *variables, functions, classes, interfaces, etc*. 

As the [TypeScript Documentation] (http://www.typescriptlang.org/docs/handbook/modules.html) says:
>Modules are executed within their own scope, not in the global scope; this means that variables, functions, classes, etc. declared in a module are not visible outside the module unless they are explicitly exported

## Export

Basically there are two ways of exporting a declaration (a variable, function, type alias, interface).

This first example, we see that the key word **export** prepends the declaration of an interface:

```typescript
export interface
```

