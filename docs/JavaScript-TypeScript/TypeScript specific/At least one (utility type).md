
## Description

Small utility type that takes list of properties and makes sure that at least one of them is present

## Code

```javascript
type AtLeastOne<T, U = { [K in keyof T]: Pick<T, K> }> = Partial<T> & U[keyof U];
```

## Usage

```javascript
interface SomeInterface {
  mainProperty: AtLeastOne<{
    inner1: string;
    inner2: number;
    inner3: string[];
  }>;
}
```


* all three `innerX` properties are optional:

	![[Pasted image 20231026064217.png]]

* if no `innerX` property is provided:

	![[Pasted image 20231026064018.png]]

* if only one (and any) `inner` property is provided then there are no issues:

	![[Pasted image 20231026064308.png]]
