## Description 

Create type from an existing array values. The same approach can be used with objects as well - type from the keys of an object (`Object.keys`)

## Code

```ts
const weekdayNames = [
    "monday",
    "tuesday"
] as const

type Weekday = typeof weekdayNames[number]
```

![[Pasted image 20230816045349.png]]