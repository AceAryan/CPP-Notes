```cpp
#include<iostream>
#include"log.h"
class Player {
public:
	int x, y;
	int speed;
	void Move(int xa, int ya) {
		x += xa * speed;
		y += ya * speed;
	}
};
int main() {
	Player Ace;
	Ace.x = 2;
	Ace.y = 5;
	Ace.speed = 10;
	std::cout << Ace.x << " "<< Ace.y << " "<< Ace.speed << std::endl;
	Ace.Move(3, 4);
	std::cout << Ace.x << " "<< Ace.y << " "<< Ace.speed << std::endl;
	std::cin.get();
}	
```

## Writing a Class

```cpp
#include<iostream>

class Log {
public:
	const int LogLevelError = 0;
	const int LogLevelWarning = 1;
	const int LogLevelInfo = 2;
private:
	int m_LogLevel = LogLevelInfo;
public:
	void SetLevel(int level) {
		m_LogLevel = level;
	}
	void Error(const char* message) { 
		if (m_LogLevel >= LogLevelError) {
			std::cout << "[ERROR]: " << message << std::endl;
		}
	}
	void Warn(const char* message) { 
		if (m_LogLevel >= LogLevelWarning) {
			std::cout << "[WARNING]: " << message << std::endl;
		} 
	}
	void Info(const char* message) { 
		if (m_LogLevel >= LogLevelInfo) {
			std::cout << "[INFO]: " << message << std::endl;
		} 
	}
};
int main() {
	Log log;
	log.SetLevel(log.LogLevelWarning);
	log.Warn("Hello!");
	log.Error("Error");
	log.Info("Info");
	std::cin.get();
	return 0; 
}
```
