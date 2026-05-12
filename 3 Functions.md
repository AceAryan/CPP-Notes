Block of Code to perform a specific task

**General Function Template:**
```cpp
(return value) function (parameter){
	body;
	return ___;}
```


```cpp
int Multiply(int a, int b) {
	return a * b;	
}

void MultiplyAndLog(int a, int b) {
	int result = Multiply(a, b);
	std::cout << result << std::endl;
}

int main() {
	MultiplyAndLog(5, 4);
	MultiplyAndLog(4, 2);
	MultiplyAndLog(2, 7);

	std::cin.get();
}
```

## Log.cpp :

```cpp
#include<iostream>
#include "log.h"

void Log(const char* message) {
	std::cout << message << std::endl;
}

void InitLog() {
	Log("Initializing Log");
}
```
