It finds a block of memory big enough for our requirement, then gived us a [[9 Pointers|pointer]] to that block of memory.

- Difference b/w Malloc : Malloc does not call the [[15 Constructor|Constructor]], just allocates memory while New does both. 

```cpp
#include<iostream>
#include<string>
using String = std::string;
class Entity {
private:
	String m_Name;
public:
	Entity(): m_Name("Unknown"){}
	Entity(const String& name): m_Name(name) {}
	const String& GetName() const { return m_Name; }
};
int main() {
	int* a = new int[50]; // 200 bytes
	Entity* e = new Entity();
	Entity* e1 = new Entity[50];
	delete[] a;
	delete e;
	delete[] e1;
	std::cin.get();
}
```
