"this" Keyword is a [[9 Pointers|Pointer]] to the current Instance

```cpp
#include<iostream>
#include<string>
void printEntity(const Entity& e) {
	//Print
}
class Entity {
public:
	int x, y;
	Entity(int x, int y) {
		//Entity* e = this;
		this->x = x;
		this->y = y;
		printEntity(*this);
		//delete this; don't do this
	}
	int GetX() const {
		const Entity* e = this;
		return x;
	}
};
int main() {
	std::cin.get();
}
```