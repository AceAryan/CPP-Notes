**Constructor** ek special **Method** hai jo call hota hai jab bhi hum koi object banate hai

**Initialize** karne ke kaam aata hai, C++ mai by default koi variable ke liye memory assign karoge to us memory mai jo value padi hui thi wahi us [[2 Variables|variable]] ki value ban jayegi

Constructor Name = Class Name

```cpp
#include<iostream>
class Entity {
public:
	float X, Y;

	Entity(float x, float y) {
		X = x;
		Y = y;
	};
	void Print() {
		std::cout << X << ", " << Y << std::endl;
	}
};
int main() {
	Entity e1(5.0f, 10.0f);
	e1.Print();
	std::cin.get();
}
```

**Deleting** the **Default Constructor** :
```cpp
class Log() {
private:
	//Log(){} aise bhi karsakte hai
public:
	Log() = delete;
	static void write() {

	}
};
```
