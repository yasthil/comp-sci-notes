# Factory Method
Define an interface for creating an object, but let subclasses decide which class to instantiate.
Lets a class defer instantiaion to subclasses, hence we can create objects without exposing the creation logic to the client.

# When to use Factory Method
* A class can't anticipate which kind of class of objects it must create
* A calss uses its subclasses to specify which objects it creates
* You want to localize the knowledge of which class gets created

# Code
```typescript

export class FactoryDemo {
    const hogwartsHouseFactory: HogwartsHouseFactory = new HogwartsHouseFactory();
    const house1:IHogwartsHouse = hogwartsHouseFactory.getHouse("Gryffindor");
    console.log(house1.getMascot());    // "Lion"

     const house2:IHogwartsHouse = hogwartsHouseFactory.getHouse("Slytherin");
    console.log(house2.getMascot());    // "Serpent"
}

export class HogwartsHouseFactory {
    public getHouse(name: string): IHogwartsHouse {
        if(name === "Gryffindor") {
            return new Gryffindor();
        }
        else if(name === "Slytherin") {
            return new Slytherin();
        }
        else if(name === "Ravenclaw") {
            return new Ravenclaw();
        }
       return null;
    }
}

export interface IHogwartsHouse {
   public getMascot(): string;
}

export class Gryffindor implements IHogwartsHouse {
    public getMascot(): string {
        return "Lion";
    }
}

export class Slytherin implements IHogwartsHouse {
    public getMascot(): string {
        return "Serpent";
    }
}

export class Ravenclaw implements IHogwartsHouse {
    public getMascot(): string {
        return "Eagle";
    }
}

```