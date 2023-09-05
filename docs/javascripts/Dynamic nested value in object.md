
## Description

A way to get value from an object but the "path" is dynamic

## Code

```javascript
let object = {
  one: {
    two: {
      three: {
        prop: 'val'
      }
    }
  }
};

const props = ['one', 'two', 'three', 'prop'];
const nestedVal = props.reduce((a, prop) => a[prop], object);
console.log(nestedVal);
```

## Source

The source of the solution is from [StackOverflow](https://stackoverflow.com/a/59795996/159365)