# Decorator
An object that wraps around other objects to add new features/behaviours.
* Decorators expand the functionality of an instance of a class without changing the class code.
* Provide more flexibility than static inheritance
* Work behind the scenes and are transparent to the interface

# When to use the Decorator Pattern?
* Extension by subclassing is impractical
    * Sometimes you want to add responsibilities to an individual object and not to an entire class
* Add features/behaviours that can be withdrawn

# Sample code
```typescript
// Harry Potter refrences from here: https://harrypotter.fandom.com/wiki/Patronus_Charm

// Client
class Wizard {
    // ...
    const spell: ISpell = new Patronus();
    const corporealPatronus = new PatronusDecorator(spell);
    corporealPatronus.cast();
    // ...
}

// Component
interface ISpell {
    public cast(): void;
}

// Concrete component
class Patronus implements ISpell {
    public cast(): void {
        // conjure the patronus charm
    }
}

// Base Decorator
class SpellDecorator implements ISpell {
    protected _spell: ISpell;    
    public cast(): void {
        this._spell.cast();
    }
    constructor (spell: ISpell): void {
        this._spell = spell;
    }    
}

// Concreate Decorator
class PatronusDecorator extends SpellDecorator {
    public cast(): void {
        super.cast();
        this._produceAnimalForm();
    }

    private _produceAnimalForm():void {
        // produce the guardian animal for who ever conjured the spell
    }
}

```


# Implementation 
### 1. Interface Conformance
* A decorator object's interface must conform to the interface of the component it decorates

### 2. Keep the Component classes light weight
* Ths `Component` class should be define the high level interface and no other functions.
* Keep it light and simple
* A complex `Component` class might make a `Decorator` too costly to use in quantity

### 3. Changing the 'skin' of an object VS its 'guts'
* Decorator classes should act as a layer of 'skin' over an object
* If there's a need to chagne the object's guts, use the Strategy pattern
