# Promises 

* We can specify the return type of the promises in case it's resolved
* In catch blocks we can simply call `console.error` without arguments and it will print the reject error

```ts
const prom: Promise<number> = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve(10);
    }, 1000);
    reject("Reject error");
});

const foo = () => {
    return prom;
};

foo()
    .then((value) => {
        console.log(value + 2);
    })
    .catch(console.error);
```