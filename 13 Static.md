```cpp
#include<iostream>
int s_variable = 5;
void fun() {

}
int main() {
	std::cout << s_variable << std::endl;
	std::cin.get();
}
```

Output was **5** not **10**  

**Static** bas usi translation unit ko dikhega, bahar walon ko (globally) nah dikhega
### Static File:

```cpp
static int s_variable = 10;
static void fun() {

}
```

- Why to use Static?
	- Same Reason as using Private 
	- Global define karoge to baadme problems aa sakti hai jab wo saare translation units ke across check karega

# Static for Classes and Structs

- Static Methods cannot access Non-Static Variables
	- Same as writing the Method outside of the class

```cpp
static void print(entity e) {
	std::cout << "X: " << e.x << ", Y: " << e.y << std::endl;
}
```

```cpp
static void print() {
	std::cout << "X: " << e.x << ", Y: " << e.y << std::endl;
}
```

```cpp
struct entity {
	 static int x, y;

	static void print() {
		std::cout << "X: " << x << ", Y: " << y << std::endl;
	}
};
```

The 2nd and 3rd Code blocks are essentially the same while writing methods.
When you create a Method in a [[11 Classes|Class]], the Class passes some hidden parameters on its own.