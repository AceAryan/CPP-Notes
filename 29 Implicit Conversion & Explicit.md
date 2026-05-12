Implicitly converts **Members** to construct an **Object**

If used **Explicit Keyword** ( works in front of [[15 Constructor|Constructor]] ) , then the constructor loses this functionality and you have to explicitly construct the object each time

```cpp
#include<iostream>
#include<string>	
class Entity {
private:
	std::string m_Name;
	int m_Age;
public:
	Entity(const std::string& name)
		: m_Name(name), m_Age(-1) { }
	/*explicit*/ Entity(int age)
		:m_Name("Unknown"), m_Age(age) { }
};
void printEntity(const Entity& entity) {
	//Printing
}
int main() {
	printEntity(22); // makes an entity and prints
	printEntity("Aryan"); // does not work because it is not a std::string, just a const char array, wrap inside constructor of class or std::string
	Entity a = "Aryan"; //Implicitly converting
	Entity b = 22;

	std::cin.get();
}
```