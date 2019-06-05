## Pointer

Pointer stores memory address of another value located in computer memory.
A pointer *references* a location in memory, and obtaining the value
stored at that location is known as *dereferencing* the pointer.

### Example
```cpp
int main(){
    int a = 5;
    int *p = NULL;

    p = &a;
    cout << "[" << p << "] " << *p << endl;
    *p = 6;
    cout << "[" << p << "] " << *p << endl;
    return 0;
}
```
Output:
```
[0x7ffefc6f120c] 5
[0x7ffefc6f120c] 6
```
``*`` in front of a pointer dereference it to the value at that address.
We stored the address by ``p = &a`` and update value at that address
by ``*p = 6``, yeah it works kinda like an alias.

### Example
```cpp
int main(){
    int arr[5] = {1, 2, 3, 4, 5};
    int *p = arr;
    
    cout << "[" << p << "] " << *p << endl;
    p += 2;
    cout << "[" << p << "] " << *p << endl;
    
    return 0;
}
```
Output:
```
[0x7ffca10577f0] 1
[0x7ffca10577f8] 3
```

Notice how memory address is also incrementing by ``2*4`` because ``int`` value
takes ``4 bytes`` of memory and we are incrementing by ``2``;

You could test using other data structures in C++ which do not stores value
consecutively.

\- Al
