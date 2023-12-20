
## Description

Small utility type that can be used to keep only the provided properties required
## Code

```javascript
export type Required<T, K extends keyof T> = T & { [P in K]-?: T[P] };

export type KeepRequired<T, K extends keyof T> = Pick<T, Exclude<keyof T, K>> & Required<T, K>;
```

## Usage

```javascript
interface BaseType {
  id?: string;
  name?: string;
  description?: string;
}
```

Using the `KeepRequired` utility type `name` will be keep required:

```javascript
type MakeRequired = KeepRequired<BaseType, "name">;
```


![[Pasted image 20231220212123.png]]