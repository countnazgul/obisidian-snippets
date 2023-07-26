## Description

Define singleton class in TypeScript

## Code

```javascript
export class SomeClass {
  static instance: SomeClass;
  public someVariable: number = 0;
 
  constructor() {
    //
  }

  public static getInstance(): SomeClass {
    if (!SomeClass.instance) {
      SomeClass.instance = new SomeClass();
    }
    return SomeClass.instance;
  }

  public setVariable() {
    this.someVariable++;
  }

  public getVariable() {
    return this.someVariable;
  }
}
```

Usage
```javascript
import { SomeClass } from "./SomeClass.ts";

const someClassInstance = SomeClass.getInstance();
const anotherClassInstance = SomeClass.getInstance();

someClassInstance.setVariable();

const test = anotherClassInstance.getVariable();

console.log(test);
// 1
```
