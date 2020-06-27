# Observer
Lets you define a subscription mechanism to notify multiple objects about any events they are subscribed to, or observing.

# When to use the Observer Pattern?
* When you want certain objects to be notified when something occurs on another object
* You only want the interested/subscribed objects to be notified

# Sample Code

```typescript

class Publisher {
    private _subscribers: ISubscriber [];
    public addSubscriber(subscriber: ISubscriber);
    public removeSubscriber(subscriber: ISubscriber);
}

interface ISubscriber {
    public notify(state:string):void;
}

class Subsciber implements ISubscriber {
    public notify(state:string):void {
        console.log(state);
    }
}

```
