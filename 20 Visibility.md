3 Keywords - Private, Protected, Public
[[Friend]] can access the Private Members of the [[11 Classes|Class]]

1. **Private** : Only Class itself and Friends can access these 
2. **Protected** : Class itself and Derived Subclasses can access these
3. **Public** : Everyone can access these

Useful for communicating your Code to other people or yourself.
Find the Intended way of using that Class.

```cpp
#include<iostream>
#include<string>
class Entity {
private:
	int X, Y;
public:
	Entity() {
		X = 0;
	}
};
class Player : public Entity {
	//can't access X,Y from here also
};
int main() {
	Entity e; 
	std::cin.get();
}
```
