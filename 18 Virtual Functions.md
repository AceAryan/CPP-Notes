Virtual Functions are used to override the function of Base Class during Runtime. ( Runtime [[Polymorphism]] / Late Binding )

Basically, pehle case mai jab compile ho raha tha to e aur p dono ko Entity* type ka samajh liya ( **Static Binding** / **Early Binding**), but hume chahiye tha ki jab Player ke liye print karwa rahe hai to Player ke andar wala function run hona chahiye ( kyuki wo design kara hai specifically player ke liye ) toh jab humne virtual aur override use kara to Compiler ko bola ki jab is base class ke function ko call karenge toh hold rakhna aur runtime ke duration mai uska actual type determine karke override run karna ( **Dynamic Binding** / **Late Binding** )

Before using Virtual Funcs:
```cpp
#include<iostream>
#include<string>
class Entity {
public:
	std::string GetName() { return "Entity"; }
};
class Player : public Entity {
private:
	std::string m_Name;
public:
	Player(const std::string& name)
		: m_Name(name) { }
	std::string GetName() { return m_Name; }
};
void printName(Entity* entity) {
	std::cout << entity->GetName() << std::endl;
};
int main() {
	Entity* e = new Entity();
	std::cout << e->GetName() << std::endl;
	Player* p = new Player("Aryan");
	std::cout << p->GetName() << std::endl;
	Entity* entity = p;
	std::cout << entity->GetName() << std::endl;
	return 0;
}
```

After using Virtual Fxns :
```cpp
#include<iostream>
#include<string>
class Entity {
public:
	virtual std::string GetName() { return "Entity"; }
};
class Player : public Entity {
private:
	std::string m_Name;
public:
	Player(const std::string& name)
		: m_Name(name) { }
	std::string GetName() override { return m_Name; }
};
void printName(Entity* entity) {
	std::cout << entity->GetName() << std::endl;
};
int main() {
	Entity* e = new Entity();
	printName(e);
	Player* p = new Player("Aryan");
	printName(p);
	std::cin.get();
	return 0;
}
```

- **Vtable** create hota hai jo store karta hai *array* of each virtual fxn pointer ( uske aur uske base classes ke )
- **Vptr** ek *hidden data member* jaise milta hai sabhi *objects* ko us class ke. Ye point karta hai us Object ke actual type ke **Vtable** ko 

Virtual Fxn ka [[16 Destructor|Destructor]] **humesha Virtual** hona chahiye.
Virtual [[15 Constructor|Constructor]] nahi bana sakte.