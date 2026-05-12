- Evil twin of [[15 Constructor|Constructor]]
- Runs every time when you delete an object
- To Uninitialize or Free Memory 
- Destructor Name = ~Class Name

```cpp
#include<iostream>
class Entity {
public:
	float X, Y;

	Entity() {
		X = 0.0f;
		Y = 0.0f;
		std::cout << "Created Entity!" << std::endl;
	};
	~Entity() {
		std::cout << "Destroyed Entity!" << std::endl;
	}
	void Print() {
		std::cout << X << ", " << Y << std::endl;
	}
};
void Function() {
	Entity e;
	e.Print();
}
int main() {
	Function();
	std::cin.get();
}
```
