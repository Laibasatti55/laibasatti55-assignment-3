//CODE1
#include <iostream>

using namespace std;

// Abstract base class
class Shape {
public:
    // Pure virtual function
    virtual double calculateArea() const = 0;

 //destructor
    virtual ~Shape() {}
};

//derived class
class Circle : public Shape {
private:
    double radius;

public:
    Circle(double r) : radius(r) {}

    double calculateArea() const override {
        return 3.14159 * radius * radius;
    }
};

class Rectangle : public Shape {
private:
    double width;
    double height;

public:
    Rectangle(double w, double h) : width(w), height(h) {}

   
    double calculateArea() const override {
        return width * height;
    }
};

int main() {
    // Create instances /objects of Circle and Rectangle
    Circle circle(5.0);
    Rectangle rectangle(4.0, 6.0);


    cout << "Area of the circle: " << circle.calculateArea() << endl;
    cout << "Area of the rectangle: " << rectangle.calculateArea() << endl;

    return 0;
}
