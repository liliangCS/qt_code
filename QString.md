# 简介

QString 是 Qt 框架中用于处理字符串的类，提供了丰富的操作方法。以下是一些常见的 QString 操作及其示例代码：

### 1. 创建和初始化 QString

```cpp
QString str1;  // 创建一个空字符串
QString str2("Hello, world!");  // 直接初始化
QString str3 = "Hello, Qt!";  // 赋值初始化
```

### 2. 字符串连接

```cpp
QString str4 = str2 + " " + str3;  // 使用 + 连接字符串
str4.append(" How are you?");  // 使用 append() 方法
```

### 3. 比较字符串

```cpp
bool isEqual = (str2 == str3);  // 检查两个字符串是否相等
int comparisonResult = str2.compare(str3);  // 比较两个字符串
```

### 4. 大小写转换

```cpp
QString upperStr = str2.toUpper();  // 转换为大写
QString lowerStr = str3.toLower();  // 转换为小写
```

### 5. 查找和替换

```cpp
int index = str2.indexOf("world");  // 查找子字符串的位置
str2.replace("world", "Qt");  // 替换子字符串
```

### 6. 提取子字符串

```cpp
QString subStr1 = str2.mid(0, 5);  // 提取从索引0开始的5个字符
QString subStr2 = str3.left(5);  // 提取左边5个字符
QString subStr3 = str3.right(3);  // 提取右边3个字符
```

### 7. 字符串长度

```cpp
int length = str2.length();  // 获取字符串长度
```

### 8. 字符访问

```cpp
QChar firstChar = str2.at(0);  // 获取第一个字符
str2[0] = 'h';  // 修改第一个字符
```

### 9. 字符串分割

```cpp
QStringList list = str4.split(" ");  // 按空格分割字符串
```

### 10. 去除空白字符

```cpp
QString trimmedStr = str4.trimmed();  // 去除首尾空白字符
QString simplifiedStr = str4.simplified();  // 去除多余空白字符
```

### 11. 格式化字符串

```cpp
QString formattedStr = QString("Name: %1, Age: %2").arg("Alice").arg(30);  // 格式化字符串
```

### 12. 转换为数字

```cpp
QString numStr = "12345";
int num = numStr.toInt();  // 转换为整数
double dnum = numStr.toDouble();  // 转换为浮点数
```

### 13. 转换为其他类型

```cpp
QString boolStr = "true";
bool boolean = (boolStr.toLower() == "true");  // 转换为布尔值
```

### 14. 判断字符串是否为空

```cpp
bool isEmpty = str1.isEmpty();  // 判断字符串是否为空
bool isNull = str1.isNull();  // 判断字符串是否为null
```

### 15. 字符串编码转换

```cpp
QByteArray utf8Str = str2.toUtf8();  // 转换为 UTF-8 编码
QByteArray latin1Str = str2.toLatin1();  // 转换为 Latin-1 编码
```

### 16. 转换为标准字符串

```cpp
std::string stdStr = str2.toStdString();  // 转换为 std::string
std::wstring stdWStr = str2.toStdWString();  // 转换为 std::wstring
```
