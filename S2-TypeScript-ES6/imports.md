# Imports

We can import things from other files using destructuration and exporting with `export` keyword.

```ts
// File A
export class Class{


}
```

```ts
// File B, same dir as file A
import {Class} from './A'
```