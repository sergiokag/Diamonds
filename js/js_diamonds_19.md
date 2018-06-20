# WeakMap and WeakSet

WeakSet is a special kind of Set that 

**does not prevent JavaScript 
from removing its items from memory.** 

WeakMap is the same thing for Map.

As we know from the chapter Garbage collection,
JavaScript engine stores a value in memory while it is 
**reachable** (and can potentially be used).

For instance:

`
let john = { name: "John" };

// the object can be accessed, john is the reference to it

// overwrite the reference
john = null;

// the object will be removed from memory
`

Usually, properties of an object or elements
of an array or another data structure 
are considered reachable and kept in memory 
while that data structure is in memory.

In a regular Map, 
it does not matter if we store an object as a key or as a value.
**It’s kept in memory even if there are no more references to it.**

For instance:

`
let john = { name: "John" };

let map = new Map();
map.set(john, "...");

john = null; // overwrite the reference

// john is stored inside the map
// we can get it by using map.keys()
`

With the exception of WeakMap/WeakSet.

**WeakMap/WeakSet does not prevent the object removal from the memory.**

The first difference from Map is that its keys must be objects, not primitive values.
Now, , if we use an object as the key in it,
and there are no other references to that object – 
it will be removed from memory (and from the map) automatically.

WeakMap does not support methods keys(), values(), entries(), we can not iterate over it. So :

WeakMap has only the following methods:

  * weakMap.get(key)
  * weakMap.set(key, value)
  * weakMap.delete(key, value)
  * weakMap.has(key)

WeakSet behaves similarly:

  * It is analogous to Set, but we may only add objects to WeakSet (not primitives).
  * An object exists in the set while it has reachable from somewhere else.
  * Like Set, it supports add, has and delete, but not size, keys() and no iterations.
  

WeakMap and WeakSet are used as “secondary” data structures in addition to the “main” object storage. 
Once the object is removed from the main storage, so it only stays in WeakMap/WeakSet, they clean up automatically.
  

  
  

