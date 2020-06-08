# Builder
Separate the construction of a complex object from its representation so that the same construction process can create different representations.

# When to use Builder
* When the algorithm for creating complex objects should be independent of the parts that make up the object and how they are assembled
* The construction process must allow different representation for the object that is constructed
* The building process can broken down into discrete steps


# Structure

## Builder
* Specifies an interface for creating parts of a Product object

## Concrete Builder
* Constructs and assembles parts of the product by implementing the Builder interface

## Director
* Has a reference to the Builder
* Constructs the object using the Builder interface

## Product
* Represents the complex object under construction
* Includes calsses that define the individual parts
* Provides interfaces for assembling the parts

# Code

```typescript

// Builder
export interface IBuilder {    
    public buildHandle(): void;
    public buildGrip(): void;
    public buildBrissels(): void;
    public setSpeed(speed: number): void;
}

// Concrete Builders
export class Numbus2000Builder implements IBuilder {
    private _result: Nimbus2000;
    public getResult(): Nimbus2000 { return this._result; };
    public buildHandle(): void {}
    public buildGrip(): void {}
    public setSpeed(speed: number): void;
}

export class FireBoltBuilder implements IBuilder {
    private _result: FireBolt;
    public getResult(): FireBolt { return this._result; };
    public buildHandle(): void {}
    public buildGrip(): void {}
    public buildBrissels(): void {}
    public setSpeed(speed: number): void;
}


// Products
export class FireBolt {}
export class Nimbus2000 {}

// Director
export class Director {    
    public makeFireBolt(builder: IBuilder): void {
        builder.buildHandle();
        builder.buildGrip();
        builder.buildBrissels();
        builder.setSpeed(99999999);
    }
    public makeNumbus2000(builder: IBuilder): void {
        builder.buildHandle();
        builder.buildGrip();
        builder.buildBrissels();
        builder.setSpeed(50000);
    }
}

// Client
class Client {
    const director: Director = new Director();
    const fireBoltBuilder: FireBoltBuilder = new FireBoltBuilder();
    director.makeFireBolt(fireBoltBuilder);
    const fireBolt: FireBolt = director.getResult();
}
```
