# Function vs arrow function

## Hoisting 

Normal functions have hoisting. The function can be called before it's declared. Arrow functions act as variables and can't be called before being declared.

## This keyword

`This` refers to the surrounding object. The context is obtained from the object.

```ts
const obj = {
    name: 'Geeks',
    greet: function() {
        console.log(this.name);
    }
};
obj.greet(); // -> Geeks
```

`This` is getting context from where the object is declared, in this case the global scope

```ts
const obj = {
    name: 'Geeks',
    greet: () => {
        console.log(this.name);
    }
};
obj.greet(); // Output: undefined (inherited from outer scope)
```

### Inside classes instead of literal objects

While inside classes it doesn't matter if function or arrow is used (except for the constructor)

## Constructor

Arrow functions can't be used as constructors with the keyword `new`