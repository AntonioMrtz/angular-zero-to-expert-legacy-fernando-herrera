# Destructuring Arrays and Objects

## Objects

```ts
const obj = {
    attr1: "attr1",
    attr2: "attr2",
};

const { attr1, attr2 } = obj;

console.log("🚀 ~ obj:", obj);
```

## Arrays

```ts
const arr = ["attr", "attr2"];

const [arr1,arr2] = arr

console.log("🚀 ~ arr1,arr2:", arr1,arr2)
```

Skipping some array values can be done with:

```ts
const arr = ["attr", "attr2"];

const [,arr2] = arr

console.log("🚀 ~ arr2:", arr2)
```