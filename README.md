remoc
=====

javascript + c/c++ remote binding

Basic Concept
----
* js (client-side)
```js
var api = new Remoc("localhost");

alert( api.sum(10,11) );
```

* c/c++ (server-side)
```c++
remoc_func<void(int,int)> sum([](int a,int b){
  return a + b;
}).glue();
```
