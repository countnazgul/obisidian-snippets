## Description

Small utility type that can be used to make property/properties optional from an existing type
## Code

```javascript
type Optional<T, K extends keyof T> = Pick<Partial<T>, K> & Omit<T, K>;
```

## Usage

```javascript
interface BaseType {
  id: string;
  name: string;
  description: string;
}
```

Using the `Optional` utility type `name` and `description` can be made optional:

```javascript
type WithOptional = Optional<BaseType, "name" | "description">;
```

![[Pasted image 20230801211905.png]]