Anything you doing while the [[3 Functions|Function]] f is running = its inside scope of f
Stack data gets deleted once outside scope
Heap allocation and deletion can be automated using [[33 Smart Pointers|Smart Pointers]]
i.e. some [[9 Pointers|pointer]] which will delete the data when the Object of the [[11 Classes|Class]] is done.

```cpp
#include<iostream>
#include<string>
class Entity {
private:
	int x;
public:
	Entity() {
		std::cout << "Created Entity!" << std::endl;
	}
	~Entity() {
		std::cout << "Destroyed Entity!" << std::endl;
	}
};
int* createArray() {
	int* array = new int[50];
	return array;
}
class ScopedPtr {
private:
	Entity* m_Ptr;
public:
	ScopedPtr(Entity* ptr) 
		:m_Ptr(ptr)
	{
	}
	~ScopedPtr() {
		delete m_Ptr;
	}
};
int main() {
	ScopedPtr e = new Entity(); // ptr will get destroyed once the object gets deleted
	std::cin.get();
}
```
