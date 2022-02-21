### Beginning 
```c++
#include <bits/stdc++.h>
using namespace std;
int main() {
// solution comes here
}
```

## Vector

### Initialise
```c++
vector<int> v = {4,2,5,3,5,8,3};
```

### Sorting
```c++
sort(v.begin(),v.end());
```

### Reverse Sorting
```c++
sort(v.rbegin(),v.rend());
```

### Using push_back
```c++
vector<int> v;
v.push_back(3); // [3]
v.push_back(2); // [3,2]
v.push_back(5); // [3,2,5]
```

* Pop from a vector 
```c++
v.pop_back();
```
* View back of vector
```c++
v.back();
```

#### size 10, initial value 0
```c++
vector<int> v(10);
```
#### size 10, initial value 5
```c++
vector<int> v(10, 5);
```
