# Object.keys, values, entries

## Iterations over data structures

For plain objects, the following methods are availiable:

* Object.keys(obj) - returns an array of keys.
* Object.values(obj) - returns an array of values.
* Object.entries(obj) - returns an array of [key, value] pairs.

```javascript
let user = {
  name: "John",
  age: 30
};

// loop over values
for (let value of Object.values(user)) {
  alert(value); // John, then 30
}
```

## Object.keys/values/entries ignore symbolic properties

Just like a for..in loop, these methods ignore 
properties that use Symbol(...) as keys.

Usually that’s convenient. 
But if we want symbolic keys too, 
then there’s a separate method **Object.getOwnPropertySymbols**
that returns an array of only symbolic keys.

Also, the method **Reflect.ownKeys(obj)** returns all keys.
