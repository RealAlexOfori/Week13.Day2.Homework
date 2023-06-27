# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

Answer: It describes situations in which something occurs in different forms.
Or also, It refers to the ability of an object to take on many forms or to be represented by multiple types.


2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

Answer: It means that we design our classes and objects in a way that allows them to exhibit polymorphic behavior. This involves creating a common interface or superclass that multiple classes can implement or inherit from, thereby enabling them to be used interchangeably.

// Superclass
class Animal {
    public void makeSound() {
        System.out.println("Animal is making a sound.");
    }
}

// Subclasses
class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Dog is barking.");
    }
}

class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Cat is meowing.");
    }
}

3. What can we use to implement polymorphism in Java?

Answer: We can use inheritance,method overriding, interfaces, and abstract classes 

4. How many 'forms' can an object take when using polymorphism?

Answer: an object can take multiple "forms" 

5. Give an example of when you could use polymorphism.

Answer: Polymorphism occurs when one class is created that extends another one. For instance, let's consider a class Animal and let Cat be a subclass of Animal . So, any cat IS an animal. Here, a Cat satisfies the IS-A relationship for its own type, Cat as well as its super class Animal , and is therefore polymorphic.



# Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming?

Answer: In object-oriented programming, composition refers to a design principle that allows objects to be composed of other objects as their parts or components.
It is a way of creating complex objects by combining simpler objects, forming a "has-a" relationship. 

7. When would you use composition? Provide a simple example in Java.

Answer: Composition is used in scenarios where one object needs to be composed of other objects as its parts or components. 

class Engine {
    public void start() {
        System.out.println("Engine started.");
    }
}

class Car {
    private Engine engine;

    public Car() {
        engine = new Engine(); // Composition: Car has an Engine
    }

    public void startCar() {
        engine.start();
        System.out.println("Car started.");
    }
}



8. Give a difference between composition and aggregation?

Answer: Composition has a strong ownership and dependency between objects, where the composed objects cannot exist independently. Aggregation represents a weaker relationship, where the composed objects can exist independently and have a looser dependency on the parent object. 

9. What is/are the advantage(s) of using composition/aggregation?

Answer: Composition and aggregation offer advantages such as code reusability, encapsulation, flexibility, modularity, clearer object relationships, code organization, object independence, scalability, extensibility, and reduced complexity.

10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?

Answer: When an object that utilizes composition is destroyed, the composed objects that are part of it are also destroyed. This is because in composition, the composed objects are owned and managed by the parent object.

11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?

Answer: When using aggregation, the composed objects that are part of an object are not automatically destroyed when the parent object is destroyed. In aggregation, the composed objects can exist independently of the parent object and have their own lifecycle.