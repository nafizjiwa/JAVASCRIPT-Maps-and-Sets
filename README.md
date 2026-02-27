# JAVASCRIPT-Maps-and-Sets
Sets store **unique values of any type**, while WeakSets store **only objects** and hold them **weakly**, allowing automatic garbage‑collection. Sets are fully featured and iterable; WeakSets are limited, non‑iterable, and used mainly for memory‑efficient tracking of object references.

---

### 🌳 Sets in JavaScript
A Set is a collection of **unique values**—no duplicates allowed. It accepts **any data type**, including primitives and objects.

```js
const treeSet = new Set(["Baobab", "Jackalberry", "Mopane Tree"]);
console.log(treeSet);
// Set(3) {'Baobab', 'Jackalberry', 'Mopane Tree'}
```

Key operations:
- `add(value)` — adds a value  
- `delete(value)` — removes a value  
- `has(value)` — checks existence  
- `clear()` — removes all values  
- `size` — number of items  
- Iterable with `forEach`, `keys`, `values`, `entries`

Duplicate values are ignored:
```js
treeSet.add("Baobab"); // ignored
```

---

### 🪶 WeakSets in JavaScript
A WeakSet stores **only objects** (no strings, numbers, etc.).  
Its references are **weak**, meaning objects are removed automatically when no other references exist.

```js
const ws = new WeakSet();
ws.add({ name: "Baobab" });
```

Important differences:
- Cannot store primitives  
- Not iterable (no `forEach`, no loops)  
- Only supports: `add()`, `delete()`, `has()`  
- Used for memory‑safe tracking of objects

Attempting to add a primitive:
```js
ws.add("Alan"); 
// Error: Invalid value used in weak set
```
---

### 📊 Set vs. WeakSet Comparison

| Feature | Set | WeakSet |
|--------|------|----------|
| Allowed values | Any type | Objects only |
| Reference type | Strong | Weak |
| Iterable | Yes | No |
| Methods | Many (`add`, `delete`, `has`, `keys`, `values`, `size`) | Only `add`, `delete`, `has` |
| Use case | Unique collections, deduping arrays | Memory‑efficient object tracking |

---

Sets are general‑purpose collections of unique values, while WeakSets are specialized tools for managing object references without preventing garbage collection.
