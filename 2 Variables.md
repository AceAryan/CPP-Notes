- Stored in **Memory** -> Stack / Heap
- Main difference between Variables -> ***Size***
- `sizeof(variable datatype)` gives its Byte

| Variable Type | Size in Bytes         | Generally used for    |
| ------------- | --------------------- | --------------------- |
| char          | 1                     | storing characters    |
| short         | 2                     |                       |
| int           | 4                     |                       |
| long          | 4                     |                       |
| long long     | 8                     |                       |
| float         | 4                     | 5.5f -> float         |
| double        | 8                     | 5.5 -> double         |
| bool          | 1 ( uses only 1 bit ) | 0 , Anything except 0 |
- *Unsigned* -> No sign -> Can store larger no. in it
- eg. signed int -> $-2^{31}$ to $2^{31}$    ,  unsigned int -> $0$ to $2^{32} - 1$


```cpp
#include<iostream>
 
int main() {
	int variable = 8;
	unsigned int var = 5;

	//char, short , int ,long, long long

	std::cout << variable << std::endl;
	std::cin.get();
}
```

