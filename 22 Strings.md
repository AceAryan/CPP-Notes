[[21 Arrays|Array]] of Characters
- **ASCII** -> **Unicode**
- *UTF-8* (8 bits) , *UTF-16* (16 bits) , **Unicode Translation Formats** i.e. Instruction for transforming the Unicode no. to binary for machine.
1 Byte Chars => Only English for now

' ' -> Char
" " -> Char Pointer
###### String Literals ( Absolutely Immutable )
- Anything inside " " 
- **Const char** Array
- e.g. "Hello"
###### Const Char*
- Cannot Change the Character Data ( string )
- Can point it to some other Character Data ( string )
###### Char*
- Can change Character Data ( string )
- Can point it to some other Character Data ( string )
###### std::String
- Mutable by default
- Can add const ( `const std::String name = "Aryan"` ) to make the String immutable

String copying is slow, When passing string to a [[3 Functions|function]] always pass as a **Const Reference**, also promising not to modify inside the function.

```cpp
#include<iostream>
#include<string>
void printString(const std::string& string) {
    std::cout << string << std::endl;
}
int main() {
    const char* name = "Aryan";
    char name2[6] = { 'A','r','y','a','n','\0' };
    std::cout << name2 << std::endl;
        //Using std::string
    std::string name = "Aryan";
    std::cout << name.size() << std::endl;
    std::string name2 = std::string("Abc") + " 123"; 
    //otherwise error if directly concatenate in same line
    printString(name);
    std::cin.get();
}	
```

# String Literals

Anything between " "
Has a Null Character '\0' in the end.
stored in a Read-Only section

```cpp
#include<iostream>
#include<string>
#include<stdlib.h>
int main() {
	using namespace std::string_literals;

	std::string name0 = "Cherno"s + "hello";
	const char* example = R"(Aryan   
		A
		B
		C)";  //R for Multi Line Strings
	const char* name = "Aryan"; //1Byte
	const wchar_t* name2 = L"Cherno"; //2Byte (Wide String)
	const char16_t* name3 = u"Cherno"; //2Byte
	const char32_t* name4 = U"Cherno"; //4Byte
	std::cout << name << std::endl;
	std::cin.get();
}
```





