# Modules

Module is an independent unit which can contain *variables, functions, classes, interfaces, etc*. 

As the [TypeScript Documentation](http://www.typescriptlang.org/docs/handbook/modules.html) says:
>Modules are executed within their own scope, not in the global scope; this means that variables, functions, classes, etc. declared in a module are not visible outside the module unless they are explicitly exported

## Export

Basically there are two ways of exporting a declaration (a variable, function, type alias, interface).

This first example, we see that the key word **export** prepends the declaration of an interface:

```typescript
export interface PlayerStats {
    points?: number;
    rebounds?: number;
}
```
**Important**: see that in the variables above, we're using the *?* mark. This tells the typescript, that this is an optional variable.

Another way to do it, is just use the key word **export** at the end of the file and in between braces declare what's being exported.
See the example:

```typescript
interface PlayerStats {
  points?: number;
  rebounds?: number;
}

export { PlayerStats }
```

Some will say that it's a better way to keep things organized, and easier to read.

Another thing that can be done, is export the declaration with another name, if necessary:

```typescript
interface PlayerStats {
  points?: number;
  rebounds?: number;
}

export { PlayerStats as PStats }
```
