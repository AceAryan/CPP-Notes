**References** are basically *alias* i.e. &ram = shyam => either you call ram or shyam its the same thing

```cpp
#include<iostream>
#include"log.h"
void Increment(int& value) {
	value++;
}
int main() {
	int a = 5;
	Increment(a);
	std::cout<<a<<std::endl;
	std::cin.get();
}
```

With references, you don't have a [[9 Pointers|Pointer]] and Content, you are the Content itself.