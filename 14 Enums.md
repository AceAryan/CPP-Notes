- Integer constant ko replace karne ke liye use karte hai
- Reading ke liye easy rehta hai ( Number ki Jagah koi text eg. 1 ki jagah Monday )
- Us variable ko bas unhi kuch values de sakte hai na ki kahi se bhi uthake koi int.

```cpp
#include<iostream>	
enum Example : unsigned char {
	A=1, B, C;
};
int a = 0;
int b = 1;
int c = 2;
int main() {
	Example value = B;
	if (value == 1) {
		//
	}
	std::cin.get();
}
```

[[11 Classes|Log Code]] written using Enums:

```cpp
#include<iostream>
class Log {
public:
	enum Level {
		LevelError=0, LevelWarning, LevelInfo,
	};
private:
	Level m_LogLevel = LevelInfo;
public:
	void SetLevel(Level level) {
		m_LogLevel = level;
	}
	void Error(const char* message) { 
		if (m_LogLevel >= LevelError) {
			std::cout << "[ERROR]: " << message << std::endl;
		}
	}
	void Warn(const char* message) { 
		if (m_LogLevel >= LevelWarning) {
			std::cout << "[WARNING]: " << message << std::endl;
		} 
	}
	void Info(const char* message) { 
		if (m_LogLevel >= LevelInfo) {
			std::cout << "[INFO]: " << message << std::endl;
		} 
	}
};
int main() {
	Log log;
	log.SetLevel(Log::LevelError);
	log.Warn("Hello!");
	log.Error("Error");
	log.Info("Info");
	std::cin.get();
	return 0; 
}
```
