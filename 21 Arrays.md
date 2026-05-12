as learnt in DSA 

```cpp
#include<iostream>
int main() {
	int example[5]; //Stack
	int* another = new int[5]; //Heap
	for (int i = 0; i < 5; i++) {
		example[i] = 2;
		another[i] = 2;
	}
	delete[] another;
	std::cin.get();
}
```
