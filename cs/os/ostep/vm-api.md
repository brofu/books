# Memory API


## Key Points


* **Which segment (stack or heap) allocation triggered with this statement?**
```
void func() {
    int *x = (int *) malloc(sizeof(int)); ...
}
```

* **In C, when is the value of `sizeof(double)` determined (compile phase or running time)?**

* **What's the behaviour of `sizeof()` with the following statements?**
```
   // with type
   sizeof(int)

   // with pointer
   int *x = malloc(10 * sizeof(int)); 
   sizeof(x)

   // with array
   int y[10]
   sizeof(y)
```

* **Consider the following statements, why no need `size` parameter in `free` API**
```
   int *x = malloc(10 * sizeof(int));
   ...
   free(x);
```

