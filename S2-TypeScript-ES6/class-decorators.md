# Class Decorators

Executes code on class declaration. Needs `experimentalDecorators` in `tsconfig.ts`. Can be useful at infrastructure level. It's used in Angular `Injectable`.


```ts
function test(target:any){
    const prototypeProps = Object.getOwnPropertyNames(target.prototype);
    console.log(prototypeProps)
}

@test
class BugReport {
    type = "report";
    title: string;

    constructor(t: string) {
        this.title = t;
    }
}
```