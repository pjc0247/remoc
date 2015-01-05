remoc
=====

javascript + c/c++ remote binding

Basic Concept
----
* js (client-side)
```js
var api = new Remoc("localhost");

alert( api.sum(10,11) ); // sync??
alert( await api.sum(10,11) ); // await??

api.sum(10,11, function(v){
  alert(v);  // async??
});
```

* c/c++ (server-side)
```c++
remoc_func<void(int,int)> sum([](int a,int b){
  return a + b;
}).glue();
```
