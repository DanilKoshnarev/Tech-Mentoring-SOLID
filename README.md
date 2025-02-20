# SOLID Принципи в Об'єктно-Орієнтованому Програмуванні

Цей репозиторій допоможе вам зрозуміти та застосувати SOLID принципи в ООП на мовах Python, C++ та Go.

## Зміст
1. Вступ до SOLID
2. Single Responsibility Principle (SRP)
3. Open/Closed Principle (OCP)
4. Liskov Substitution Principle (LSP)
5. Interface Segregation Principle (ISP)
6. Dependency Inversion Principle (DIP)
7. Приклади коду
8. Література

## Вступ до SOLID
SOLID - це набір з п'яти принципів об'єктно-орієнтованого програмування, які допомагають робити код більш зрозумілим, підтримуваним та гнучким.

## Single Responsibility Principle (SRP)
Принцип єдиної відповідальності: кожен клас повинен мати тільки одну причину для змін.

## Open/Closed Principle (OCP)
Принцип відкритості/закритості: програмні сутності повинні бути відкриті для розширення, але закриті для змін.

## Liskov Substitution Principle (LSP)
Принцип підстановки Лісков: об'єкти повинні мати можливість бути заміненими їхніми підкласами без порушення коректності програми.

## Interface Segregation Principle (ISP)
Принцип сегрегації інтерфейсів: клієнти не повинні залежати від інтерфейсів, які вони не використовують.

## Dependency Inversion Principle (DIP)
Принцип інверсії залежностей: абстракції не повинні залежати від деталей, деталі повинні залежати від абстракцій.

## Приклади коду
### Python
```python
class Report:
    def generate(self):
        pass

class PDFReport(Report):
    def generate(self):
        return "PDF Report"

class HTMLReport(Report):
    def generate(self):
        return "HTML Report"
```

### C++
```cpp
class Report {
public:
    virtual std::string generate() = 0;
};

class PDFReport : public Report {
public:
    std::string generate() override {
        return "PDF Report";
    }
};

class HTMLReport : public Report {
public:
    std::string generate() override {
        return "HTML Report";
    }
};
```

### Go
```go
package main

import "fmt"

type Report interface {
    Generate() string
}

type PDFReport struct {}

func (p PDFReport) Generate() string {
    return "PDF Report"
}

type HTMLReport struct {}

func (h HTMLReport) Generate() string {
    return "HTML Report"
}

func main() {
    var r Report = PDFReport{}
    fmt.Println(r.Generate())
}
```

## Література
1. *Clean Code: A Handbook of Agile Software Craftsmanship* by Robert C. Martin
2. *The Pragmatic Programmer: Your Journey to Mastery* by Andrew Hunt and David Thomas

## Про мене
Привіт! Мене звати **Кошнарьов Данил**, я софтвер девелопер та розробник ПО. Моя мета - допомогти вам освоїти SOLID принципи та стати кращими програмістами.

## Зворотний зв'язок
Якщо у вас є питання чи пропозиції, не соромтеся зв'язатися зі мною.
