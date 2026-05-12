```cpp
#include<iostream>
#include"log.h"
int main() {
	for (int i = 0; i < 5; i++) {
		if (i % 2 == 0)
			continue; //break (same result in this case, loop ends)	
		// return ends the function
		Log("Hello World!");
		std::cout << i << std::endl;
	}
	std::cin.get();
}
```