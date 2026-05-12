Used for [[3 Functions|Function]] Declaration

`#pragma once` *(Header Guard)* ensures the Header file is included only once in the translation unit
Traditional Way of doing pragma once was: 
```cpp
#ifndef
#define

___
___

#endif
```

`#include <>` -> Files in the Include Path / Directory
`#include " "` -> From Current directory, relative 
*Can use " " for everything though*

Header files with **C STL** -> **.h** or other extensions
		       **C++ STL** -> no extensions

```cpp
#include<iostream>
#include "log.h"

int main() {
	InitLog();
	Log("Hello World!");
	std::cin.get();
}
```

## Log.h :

```cpp
#pragma once 

void InitLog();
void Log(const char* message);
```
