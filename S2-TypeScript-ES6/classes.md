# Classes


* Declare `public attr2: number` parameter in the class constructor for not having to assign a value to `attr2` like `this.attr2=attr2`.
* Private class attrs can be accessed only inside the class. Public ones in the other hand can be accessed from outside the class.

```ts
class Class {
    attr1: string;

    constructor(attr1: string, public attr2: number, private attr3: number) {
        this.attr1 = attr1;
        // attr2 and attr3 are set automatically as class attributes with same name
    }
    foo() {
        console.log(this.attr2 + this.attr3); // attr3 can be used in the class because it's private
    }
}

const obj = new Class("attr1", 10, 100);

console.log(obj.attr1);
console.log(obj.attr2);
console.log(obj.attr3); // ! Error -> it's private
```