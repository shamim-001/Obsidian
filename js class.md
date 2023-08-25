#js #js-concept #class #oop 
Classes are a way to create objects that have similar characteristics and behaviors.

**[[static method]]


```js
// Class(ES6) 
// Class is a template for creating objects

class Animal {
  constructor(name) {
    this.name = name;
  }

  sound() {
    console.log("The animal makes a sound.");
  }

  static info() {
    console.log("This is the Animal class.");
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name);
    this.breed = breed;
  }

  sound() {
    console.log("Woof! The dog barks.");
  }

  static info() {
    console.log("This is the Dog class.");
  }
}

const animal = new Animal("Generic Animal");
const dog = new Dog("Buddy", "Labrador");

console.log(animal.name);
animal.sound();

console.log(dog.name);
console.log(dog.breed);
dog.sound();

Animal.info();
Dog.info();

```

- Classes are declared using the `class` keyword, followed by the class name.
- The ==`constructor` method is a special method that initializes class instances and is called automatically when using the `new` keyword.==
- Properties can be defined using the `this` keyword within the constructor or other class methods.
- Methods are functions defined within the class and can perform actions or calculations on the class instances or properties.
- Inheritance can be achieved using the `extends` keyword, allowing a class to inherit properties and methods from a parent class.
- Static methods are defined on the class itself and can be called without instantiating the class.
- Instances of classes are created using the `new` keyword, and properties and methods can be accessed using dot notation.
- Class hierarchy and method overriding allow for customizing behavior in derived classes.