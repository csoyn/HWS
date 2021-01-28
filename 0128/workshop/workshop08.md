# Workshop 08

### 1. 도형 만들기

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y


class Rectangle(Point):
    def __init__(self, p1, p2):   			# 변수설정 p1, p2
        self.x = abs(p1.x - p2.x)			# 가로길이
        self.y = abs(p1.y - p2.y)			# 가로길이

    def get_area(self):
        return self.x * self.y

    def get_perimeter(self):
        return (self.x  + self.y)*2 

    def is_square(self):
        if  self.x == self.y:
            return True
        else:
            return False    


p1 = Point(1, 3)
p2 = Point(3, 1)
r1 = Rectangle(p1, p2)
print(r1.get_area())
print(r1.get_perimeter())
print(r1.is_square())


p3 = Point(3, 7)
p4 = Point(6, 4)
r2 = Rectangle(p3, p4)
print(r2.get_area())
print(r2.get_perimeter())
print(r2.is_square())
```

