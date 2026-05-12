a **const** is like a : *"if I modify this, please give an error calling me an idiot because I modified a const"*, still can bypass this promise

agar kahin pe koi cheez nahi badalni to humesha use const mark kardena

```cpp
#include<iostream>
class Entity {
private:
	int m_x, m_y;
	mutable int val; // Mutable member can be modified inside const fxns
public:
	int GetX() const { // Cannot change the data 
		return m_X
	}
	int GetX() {
		return m_X;
	} // Two functions, 1 for Const reference , 1 otherwise
	void SetX(int x) {
		m_x = x;
	}
};
void PrintEntity(const Entity& e) {
	std::cout << e.GetX() << std::endl;
}
int main() {
	Entity e;
	const int MAX_AGE = 90;
	//int const* a = new int; // both are the same thing
	//const int* a = new int; // cannot modify content here	
	int* const a = new int; //can change data, cannot change where it is pointing to
	*a = 2;
	a = (int*)&MAX_AGE;
	// Broke the promise here
	std::cout << *a << std::endl;
	std::cin.get();
}
```

