Short form of [[6 Conditions and Branches|If, Else]] Statement
Can Nest but not Recommended

```cpp
#include<iostream>
static int s_Level = 1;
static int s_Speed = 2;
int main() {
	/*if (s_Level > 5)
		s_Speed = 10;
	else
		s_Speed = 5;*/
	s_Speed = s_Level > 5 && s_Level < 100 ? s_Level >10 ? 15 : 10 : 5;
	std::string rank = s_Level > 10 ? "Master" : "Beginner";
	std::cout << s_Speed << " " << rank << std::endl;
}
```
