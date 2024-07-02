# 简介

QStringList 是 Qt 框架中一个非常常用的类，用于处理字符串列表。下面是一些常见的 QStringList 操作及其示例代码：

### 1. 创建和初始化 QStringList

```cpp
QStringList list;
list << "Apple" << "Banana" << "Cherry";
```

### 2. 添加元素

```cpp
list.append("Date");
list += "Elderberry";
```

### 3. 插入元素

```cpp
list.insert(2, "Blueberry");  // 在索引2位置插入"Blueberry"
```

### 4. 访问元素

```cpp
QString firstFruit = list.at(0);  // 获取第一个元素
QString lastFruit = list.last();  // 获取最后一个元素
```

### 5. 删除元素

```cpp
list.removeAt(1);  // 删除索引为1的元素
list.removeAll("Cherry");  // 删除所有值为"Cherry"的元素
list.clear();  // 清空列表
```

### 6. 查找元素

```cpp
int index = list.indexOf("Banana");  // 返回"Banana"的索引
bool contains = list.contains("Apple");  // 检查是否包含"Apple"
```

### 7. 排序和去重

```cpp
list.sort();  // 排序
list.removeDuplicates();  // 去重
```

### 8. 转换为其他数据类型

```cpp
QStringList list = QStringList() << "one" << "two" << "three";
QString joinedString = list.join(", ");  // 转换为字符串，元素间用逗号分隔
QStringList splitList = joinedString.split(", ");  // 根据逗号重新分割成QStringList
```

### 9. 使用过滤

```cpp
QStringList filteredList = list.filter("B");  // 筛选出包含"B"的元素
```

### 10. 遍历元素

```cpp
for (const QString &fruit : list) {
    qDebug() << fruit;
}
```

### 11. 转换大小写

```cpp
QStringList upperList = list;
for (QString &str : upperList) {
    str = str.toUpper();
}

QStringList lowerList = list;
for (QString &str : lowerList) {
    str = str.toLower();
}
```

### 12. 使用 QStringListModel

QStringListModel 是一个方便的模型类，可以用于将 QStringList 数据显示在基于 MVC 的视图中，例如 QListView。

```cpp
#include <QApplication>
#include <QListView>
#include <QStringListModel>

int main(int argc, char *argv[]) {
    QApplication app(argc, argv);

    QStringList fruits;
    fruits << "Apple" << "Banana" << "Cherry";

    QStringListModel model;
    model.setStringList(fruits);

    QListView view;
    view.setModel(&model);
    view.show();

    return app.exec();
}
```
