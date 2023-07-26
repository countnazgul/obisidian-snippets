## Description

If there is an object that can have as property one type or another. For example if there is an object containing data for 

## Code

```javascript

type SomeType =
  | {
      someProperty: boolean;
      anotherProperty?: undefined;
      yetAnotherProperty?: undefined;
    }
  | {
      someProperty?: undefined;
      anotherProperty: string;
      yetAnotherProperty: string;
    };
```

After the type is defined then the object can be used like:

![[Pasted image 20230726060123.png]]

If try and mix properties from both sub-types into a single object then will get an error:
![[Pasted image 20230726060022.png]]

Will get an error if miss some of the mandatory properties of the sub-type
![[Pasted image 20230726060205.png]]

## Notes

The example is a simple one but it can be extended quite well to include more sub-types or even have common properties and different sub-types