# Adapter
Allows objects which have different interfaces communicate with each other.

Real-World Analogy: `Europe AC plug` -> `EU to U.S Adapter` -> `U.S Wall Outlet`

# When to use an Adapter
Use an Adapter when:
* You want to use existing class but it's interface does not match the one you need
* You want to create a reusable class that co-operates with unrelated or unforseen classes
    * i.e. classes that don't necessarily have compatible interfaces

# When to use an Object Adapter
Use an Object Adapter when:
* You need to use several existing subclasses, however it's impractical to adapt thier interface by inheriting each one.
* An object adapter can adapt the interface of its parent class 

# Sample Code
```typescript

// Client
class Harry {
    private _map: IParchmentMap
}

// Target
class IParchmentMap {
    public reveal(): void;
}

// Adapter
class MaraudersMapAdapter extends IParchmentMap {
    private _maraudersMap:MaraudersMap;
    public reveal(): void {
        _maraudersMap.revealUsingSpell("ISolemnlySwearThatIAmUpToNoGood");
    }
}

// Adaptee
class MaraudersMap {    
    public revealUsingSpell(incantation: string): void;
}

```