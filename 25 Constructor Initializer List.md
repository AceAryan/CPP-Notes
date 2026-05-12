Way to Initialize [[11 Classes|Class]] member [[3 Functions|functions]] inside [[15 Constructor|Constructor]]
Use this List everywhere

```cpp
#include<iostream>
#include<string>
class Example {
public:
	Example() {
		std::cout << "Created Entity" << std::endl;
	}
	Example(int x) {
		std::cout << "Created Entity with " << x << std::endl;
	}
};
class Entity {
private:
	std::string m_Name;
	int m_Score;
	Example m_Example;
public:
	Entity()
		: m_Name("Unknown"), m_Score(0), m_Example(Example(8)) //Initializer List, Write in order of Declaration
	{
		//m_Example = Example(8); //created 2 entities
	}
	Entity(const std::string& name, int score)
		: m_Name(name), m_Score(score), m_Example(Example(8))
	{
	}
	const std::string& GetName() { return m_Name; };
};
int main() {
	Entity e1("Aryan",13);
	std::cout << e1.GetName() << std::endl;
	std::cin.get();
}
```
