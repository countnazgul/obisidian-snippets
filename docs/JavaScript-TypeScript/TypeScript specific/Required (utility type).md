## Description

Small utility type that can be used to make property/properties required from an existing type
## Code

```javascript
Required<T, K extends keyof T> = T & { [P in K]-?: T[P] };
```
## Usage

```javascript
interface BaseType {
  id?: string;
  name?: string;
  description?: string;
}
```

Using the `Required` utility type `name` and `description` can be made required:

```javascript
type WithRequired = Required<BaseType, "name" | "description">;
```

![[Pasted image 20231220211843.png]]
