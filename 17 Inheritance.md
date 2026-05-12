Ek [[11 Classes|Class]] dusre Class ko extend karta hai ( like Superset )
- Base Class
	- Sub Classes which extend form this Class
	- All Sub Classes have property of Base Class along with things of their own.

```cpp
#include<iostream>
class Entity {
public:
	float X, Y;
	void Move(float xa, float ya) {
		X += xa;
		Y += ya;
	}
};
class Player :public Entity {
public:
	const char* Name;

	void printName() {
		std::cout << Name << std::endl;
	}
};
int main() {
	std::cout << sizeof(Player) << std::endl;
	Player player1{};
	player1.Move(5,5);
	player1.X = 2;
	std::cin.get();
}
```