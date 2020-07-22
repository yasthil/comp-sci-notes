# Dictionary
Represents a strongly-typed collection of key/value pairs

# Characteristics
- Strongly typed, `Dictionary<TKey,TValue>`
- Preferred over using `Hashtables`
- Internally implemented as a hash table
- Every key must be unique
- Capacity is automatically increased when as required by reallocating the interal array
- Each item is treated as a `KeyValuePair<TKey,TValue>`

# Implementation
## Remarks
- The speed of retrieval depends on the quality of the hashing algorithm of the type specified for `TKey`
- The Add method throws an exception if the new key is
- Use `TryGetValue` to get a value if you're not sure if a key exists
- `ContainsKey` can be used to test keys before inserting

## Code
```c#
Dictionary<string, string> headsOfHouses = new Dictionary<string, string>();
headsOfHouses.Add("Gryffindor", "McGonagall");
headsOfHouses.Add("Slytherin", "Snape");
headsOfHouses.Add("Ravenclaw", "Flitwick");

try
{
    headsOfHouses.Add("Ravenclaw", "Hagrid");
}
catch (ArgumentException)
{
    Console.WriteLine("An element with Key = \"Ravenclaw\" already exists.");
}

// to retrive a value
Console.WriteLine("Head of Slytherin: "+ headsOfHouses["Slytherin"]);

// When a program often has to try keys that turn out not to
// be in the dictionary, TryGetValue can be a more efficient
// way to retrieve values.
string value = "";
if (openWith.TryGetValue("Ravenclaw", out value))
{
    Console.WriteLine("For key = \"Ravenclaw\", value = {0}.", value);
}
else
{
    Console.WriteLine("Key = \"Ravenclaw\" is not found.");
}

// to iterate through the dictionary elements
foreach (KeyValuePair<string, string> headsOfHousePair in headsOfHouses)
{
    Console.WriteLine("House = {0}, Teacher = {1}", headsOfHousePair.Key, headsOfHousePair.Value);
}

```


## Complexity
|Operation|Big-O|Remarks|
|---------|-----|-------|
|Search|`O(1)`| Depends on hashing algorithm, worst case `O(n)` |
|Access|`O(1)`| Depends on hashing algorithm, worst case `O(n)` |
|Insert|`O(1)`| Depends on hashing algorithm, worst case `O(n)` |
|Delete|`O(1)`| Depends on hashing algorithm, worst case `O(n)` |

