# Offline Apps: Storing Data With Client-side Databases

Web storage (localStorage and sessionStorage) is fine for small amounts of data
such as our to-do list, but it’s an unstructured data store.

You can store keys and values, but you can’t easily search values.
Data isn’t organized or sorted in a particular way, 
plus the 5MB storage limit is too small for some applications.

For larger amounts of structured searchable data,
we need another option: web databases. 

Web databases such as 
Web SQL and IndexedDB provide an alternative to the limitations of web storage, 
enabling us to create truly offline applications.

## The State of Client-side Databases

Unfortunately, this isn’t as easy as it sounds. Browsers are split into three camps in the way they support client-side databases:

  * both IndexedDB and Web SQL (Chrome, Opera 15+)

  * IndexedDB exclusively (Firefox, Internet Explorer 10+)

  * Web SQL exclusively (Safari)
  
 
