# Singleton
A class of which there can only be one instance of. It provides a single global point of access to that instance.

# Solution
* A Singleton is responsible for tracking its own instance. To do this:
    * Make the constructor `private`
    * Provide static method/field to allow access to the only instance

# Code
* This is an example of a *Lazy* instantiation (i.e. this class will only be created when it's required).
* NB: This is not the thread-safe version
```typescript
export class Singleton {
    private static _instance: Singleton = null;
    private constructor(): void {}    

    public static getInstance(): Singleton {
        if(this._instance === null) {
            this._instance = new Singleton();
        }        
        return this._instance;
    }
}

```