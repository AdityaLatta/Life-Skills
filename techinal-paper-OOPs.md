# Object-Oriented Programming

Object-oriented programming is a programming paradigm that uses objects and classes to organize code. The essential principles of OOP are:

1. **Encapsulation**: The bundling of data, methods, or functions, into a single unit, called a class. It restricts direct access to some of the object's components, which might prevent accidental modifications.

    ```javascript
    class Car {
        constructor(brand) {
            this._brand = brand;
        }
        get brand() {
            return this._brand;
        }
        set brand(newBrand) {
            this._brand = newBrand;
        }
    }

    let myCar = new Car("Thar");
    console.log(myCar.brand); // Thar

    myCar.brand = "Mahindra";
    console.log(myCar.brand); // Mahindra
    ```

2. **Abstraction**: It hides complex implementation details and shows only the necessary functionalities. That makes interaction with the object easier.

    ```javascript
    class Vehicle {
        startEngine() {
            console.log("Engine started");
        }

        stopEngine() {
            console.log("Engine stopped");
        }
    }

    let myCar = new Car();
    myCar.startEngine(); // Engine started
    myCar.stopEngine(); // Engine stopped
    ```

3. **Inheritance**: It is a mechanism in which one class can inherit the properties and methods of another class, which allows us to code reuse and create hierarchical relationships.

    ```javascript
    class Animal {
        constructor(name) {
            this.name = name;
        }

        speak() {
            console.log(`${this.name} speaks.`);
        }
    }

    class Dog extends Animal {
        speak() {
            console.log(`${this.name} barks.`);
        }
    }

    let doggy = new Dog("Rocky");
    doggy.speak(); // Rocky barks.
    ```

4. **Polymorphism**: Different classes may respond to the same method call in different ways. Example: overriding methods in a parent class.

    ```javascript
    class Animal {
        speak() {
            console.log("Animal speaks");
        }
    }

    class Cat extends Animal {
        speak() {
            console.log("Meow");
        }
    }

    class Dog extends Animal {
        speak() {
            console.log("Woof");
        }
    }

    function makeAnimalSpeak(animal) {
        animal.speak();
    }

    makeAnimalSpeak(new Cat()); // Meow
    makeAnimalSpeak(new Dog()); // Woof
    ```

## References Links

1. **FreeCodeCamp**:
   [Object-Oriented JavaScript for Beginners](https://www.freecodecamp.org/news/object-oriented-javascript-for-beginners/ "Visit Article")

2. **Medium**:
   [Object-Oriented Programming in JavaScript with Examples](https://medium.com/@zalewski/object-oriented-programming-in-javascript-with-examples-updated-2024-0b3a90955965/ "Visit Article")
