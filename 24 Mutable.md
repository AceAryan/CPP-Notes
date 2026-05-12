2 Usecases: [[23 Const|Const]], [[Lambda]]

1. Mutable members can be changed inside Const functions inside class without breaking the code.
```cpp
#include<iostream>
#include<string>
class Entity {
private:
	std::string m_Name;
	mutable int m_DebugCount = 0;
public:
	const std::string& GetName() const {
		m_DebugCount++;
		return m_Name };
};
int main() {
	const Entity e;
	e.GetName();
	std::cin.get();
}
```

2. Can change variable passed by value inside Lambda
```cpp
#include<iostream>
#include<string>
class Entity {
private:
	std::string m_Name;
	mutable int m_DebugCount = 0;
public:
	const std::string& GetName() const {
		m_DebugCount++;
		return m_Name };
};
int main() {
	const Entity e;
	e.GetName();
	int x = 8;
	auto f = [=]() mutable { //& for reference ,= creates a local variable copy
		x++; 
		std::cout << x << std::endl;
	};
	f();
	// x=8
	std::cin.get();
}
```
