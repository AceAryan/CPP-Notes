Pure Virtual [[3 Functions|Function]]
A [[11 Classes|Class]] which only contains Unimplemented *Methods*
Acts as a *Template*
Cannot *instantiate* this Class
aka **Abstract Class**

```cpp
#include<iostream>
#include<string>	
class Printable {
public:
	virtual std::string GetClassName() = 0;
};
class Entity : public Printable{
public:
	virtual std::string GetName() { return "Entity"; }
	std::string GetClassName() override { return "Entity"; }
};
class Player : public Entity {
private:
	std::string m_Name;
public:
	Player(const std::string& name)
		: m_Name(name) { }
	std::string GetName() override { return m_Name; }
	std::string GetClassName() override { return "Player"; }
};
void printName(Entity* entity) {
	std::cout << entity->GetName() << std::endl;
};
void Print(Printable* obj) {
	std::cout << obj->GetClassName() << std::endl;
}
int main() {
	//Entity* e = new Entity();
	//printName(e);
	Player* p = new Player("Aryan");
	GetClassName(p);
	std::cin.get();
	return 0;
}
```