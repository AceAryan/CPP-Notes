[Playlist Link](https://youtube.com/playlist?list=PLlrATfBNZ98dudnM48yfGUldqGD0S4FFb&si=nBlThvh7qSmIhyoq)
## How C++ Works

- There are Preprocessing statements ( eg. `#include<iostream`)
- Main [[3 Functions|Function]] -> where the program enters / starts
- Execution happens Line by Line ( [[8 Control Flow| Control Flow]] statements can change this )
- << is [[Overloaded Operator]] -> A [[3 Functions|fxn]] only ( similar to ***print(param)*** )

**Each CPP File -> *( Compiled to Object File )* -> Obj Files -> *( Linker )* -> Creates 1 Executable ( .exe ) file**
 
```cpp
#include<iostream>
void Log(const char* message);

int main() {
	Log("Hello World!");
	std::cin.get();
}
```

## How Compiler Works

**C++ File**  -------------------------------> **Obj File** 
 *( Text )*                    ***Compile***

- Compiler -> Converts code to const. data / instructions ( Abstract Syntax Tree ) -> Machine Code

**CPP File != Translation Unit**
because you can add multiple files in 1 resulting in 1 obj file

- #### Preprocessing
	- `#include` , `#define`
	- Just copies the code of the Header File


## How Linker Works

**Obj File**  -------------------------------> **exe file** 
                ***Linking***







