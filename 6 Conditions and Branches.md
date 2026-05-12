```cpp
#include <iostream>
#include "log.h"
int main() {
	
	int x = 5;
	bool comparisonResult = x == 5;
	if (comparisonResult) {
		Log("Hello World!");
	}

	std::cin.get();
}
```

else if = nested if inside else