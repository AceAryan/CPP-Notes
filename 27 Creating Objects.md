Allocate in Stack whenever possible

Stack faster, don't have to manually allocate as well as free memory.
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
	Entity entity; //Fastest way to instantiate object, whenever you can instantiate like this, do it
	std::cout << entity.GetName() << std::endl;
	std::cin.get();
}
```

When can't do this:
1. Using inside Function then function gets destroyed as well as the object so can't use that object further
2. Not Enough space on Stack

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
	Entity* entity = new Entity("Aryan");
	e = entity;
	std::cout << entity->GetName() << std::endl;
	std::cin.get();
	delete e;
}
```
