Two Main things:
	1. Breakpoints
	2. Reading Memory

**Breakpoint :** The compiler will pause there and you can look at the *Memory* then

```cpp
#include <iostream>
#include "log.h"

int main() {
	int a = 8;
	a++;
	const char* string = "Hello";

	for (int i = 0; i < 5; i++) {
		const char c = string[i];
		std::cout << c << std::endl;
	}

	Log("Hello World!");
	std::cin.get();
}
```
