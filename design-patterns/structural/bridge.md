# Bridge
Decouples an abstraction from its implementation so that the two can vary independently.
The bridge pattern can help split a large class or a set of closely related classes into two separate hierarchies:
* Abstraction 
* Implemenation

Each of these can be developed independently of each other.

# When to use Bridge?
* You want to avoid a permanent binding between an abstraction and its implementation. 
* Implementation may be switched at runtime
* Changes in the implementation of an abstraction should have no impact on the clients

# Example
```typescript

// Client
class App {
    //...
    const android: IPlatform = new Android();
    const ui: UserInterface = new ClientUserInterface(android);
    ui.renderButtons();
    //...        
}

// Abstraction
class UserInterface {
    private _platform: IPlatform;               // forms the bridge between UserInterface and IPlatform
    public renderButtons(): void {
        this._platform.renderNativeButtons();
    }
    constructor(platform: IPlatform):void {
        this._platform = platform;
    }
}
// Refined Abstraction 
class AdminUserInterface extends UserInterface{
    public displayAdminMenu();
}
// Refined Abstraction
class ClientUserInterface extends UserInterface{
    public displayClientMenu();
}

// Implementation
interface IPlatform {
    public renderNativeButtons(): void;
    public getOperatingSystemName(): string;
}

// Concrete Implementation
class Android implements IPlatform {
    public renderNativeButtons: void() {
        // render Android buttons
    }
    public getOperatingSystemName(): string {
        return "Android";
    }
}

```