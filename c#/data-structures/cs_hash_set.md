# Hash Set (C#)
The `HashSet<T>` class provides high-performance set operations. A `Set` is a collection that containers no duplicate elements and whose elements are in no particular order

## Characteristics
* A `HashSet<T>` object's capacity automatically increases as elements are added to the object.
* Based on the model of mathematical sets and provides high-performance set operations similar to accessing the keys of the `Dictionary<TKey, TValue>` or `Hashtable` collection.
    * Can be thought of as a `Dictionary<TKey, TValue>` collection without values.

## Sample Code
# C#

```c#
HashSet<string> dangerousBeasts = new HashSet<string>();
HashSet<string> friendlyBeasts = new HastSet<string>();

dangerousBeasts.Add("Grindylow");
dangerousBeasts.Add("Obscurus");
dangerousBeasts.Add("Erumpent");

friendlyBeasts.Add("Niffler");
friendlyBeasts.Add("Bowtruckle");
friendlyBeasts.Add("Demiguise");

Console.Write("Number of friendly beasts: " + friendlyBeasts.Count);    // Number of friendly beasts: 3
Console.Write("Number of dangerous beasts: " + dangerousBeasts.Count);  // Number of dangerous beasts: 3

HashSet<string> allBeasts = new HashSet<string>();
allBeasts.UnionWith(dangerousBeasts);   // Results in {Grindylow, Obscurus, Erumpent}
allBeasts.UnionWith(friendlyBeasts);    // Results in {Grindylow, Obscurus, Erumpent, Niffler, Bowtruckle, Demiguise}

```

## Cheat Sheet
|Description|Code|Remarks|
|---------|-----|--------|
|Union|`UnionWith (IEnumerable<T>)`|Performs a set Union|
|IntersectWith|`IntersectWith (IEnumerable<T>)`|Performs mathematical intersection on `HashSet<T>` and the given collection|
