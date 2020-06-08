# Creational Patterns
These are design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.
Make a system independent of the way in which objects are created, composed and represented.

* [Singleton](./singleton.md)
* [Factory Method](./factory_method.md)
* [Abstract Factory](./abstract_factory.md)
* Builder
* Prototype

# Benefits
* Allows you to program to an interface defined by an `abstract` class
    * Let's you configuer a system with "product" objects that vary widely in structure and functionality 

## Generic Instantiation
* Objects are instantiated without having to identify a specific class type in client code. 
* Examples: `Abstract Factory`, `Factory`

## Simplicity
* Make instantiation easier
    * Callers do not have to write long complex code to instantiate and set up an object 
* Exmples: `Builder`, `Prototype` pattern

