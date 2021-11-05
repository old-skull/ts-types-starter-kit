# ts-types-starter-kit (example)

**_NOTE: You can safety delete this folder._**

In this folder you can find package in `.tgz` format and also unpacked version.
Package already installed and declared in the `package.json` via `file:package` resolution.

Feel free to open `index.ts` and play with demo.

```ts
import { ESome, ISome, TStringOrNumber } from 'ts-types-starter-kit';

const a: TStringOrNumber = 1;
const a2: TStringOrNumber = '1';
// Type '{}' is not assignable to type 'TStringOrNumber'.
const a3: TStringOrNumber = {};

const b: ISome = {
  id: 'string_id',
  createdAt: new Date(),
  updatedAt: new Date(),
};
const b2: ISome = {
  // Type 'number' is not assignable to type 'string'.
  id: 1,
  createdAt: new Date(),
  updatedAt: new Date(),
};

const c: ESome = ESome.Some1;
const c2: ESome = ESome.Some2;
// Property 'Some3' does not exist on type 'typeof ESome'. Did you mean 'Some1'?
const c3: ESome = ESome.Some3;
```
