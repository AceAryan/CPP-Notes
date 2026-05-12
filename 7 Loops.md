```cpp
#include<iostream>
#include"log.h"
int main() {
	int i = 0;
	for (; i<5; i++) {
		Log("Hello World!");
	}
	Log("------------");
	while (i < 5) {
		Log("Hello World!");
	}
	Log("------------");
	do {
		Log("Hello World!");
	} while (i < 5);
	std::cin.get();
}
```