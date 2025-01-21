# Classes

* If there are a lot of attributes to initialize in the constructor we can declare `private/public attrName` as constructor param . This will declare `attrName` as class attribute and initialize it with the value provided in the constructor. This makes declaring the attr in the class body not needed.
* Private class attrs can be accessed only inside the class. Public ones in the other hand can be accessed from outside the class.

```ts
class Class {
    attr1: string;

    constructor(attr1: string, public attr2: number, private attr3: number) {
        this.attr1 = attr1;
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