### question 1/2
(1)一个类A的成员变量，可以是其他类B的对象。
(2)类A和B没有继承关系。

比如在这个例子中：
```
self.privileges = Privileges() 
```
就是给Admin(管理员)这个class定义一个成员变量，这个成员变量是Privileges(特权)这个class的对象。Admin对Privileges没啥继承关系，只是拥有的关系。

再比如说，可以给Box这个类定义一个成员变量叫surface，是Surface这个类的对象，Box对Surface没有继承，只是拥有一个Surface类型的变量。
```
class Box:
    def __init__(self, length, width, height, material, color):
	self.length = length
        self.width = width
        self.height = height

        self.surface = Surface(material, color)

class Surface:
    def __init__(self, material, color):
	self.material = material
        self.color = color

```
