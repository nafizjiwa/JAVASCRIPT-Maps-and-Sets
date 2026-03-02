# JAVASCRIPT-Maps-and-Sets

WeakSets store **only objects**, non‑iterable,
---
### 🌳 Sets in JavaScript
- A collection of stored **unique values of any type**, iterable.

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
- WeakSets store **only objects not primitives**, non‑iterable
- Only supports: `add()`, `delete()`, `has()`  
```js
const ws = new WeakSet();
ws.add({ name: "Baobab" });
```

Attempting to add a primitive:
```js
ws.add("Alan"); 
// Error: Invalid value used in weak set
```
### 📊 Set vs. WeakSet Comparison

| Feature | Set | WeakSet |
|--------|------|----------|
| Allowed values | Any type | Objects only |
| Reference type | Strong | Weak |
| Iterable | Yes | No |
| Methods | Many (`add`, `delete`, `has`, `keys`, `values`, `size`) | Only `add`, `delete`, `has` |
| Use case | Unique collections, deduping arrays | Memory‑efficient object tracking |

---

### 🗺️ What a Map Is  
- A **Map** is stored collection of key‑value **any type of key**, is **fully iterable**, and exposes its **size property**
---

### 🧩 What a WeakMap Is  
- A **WeakMap** stores **only object keys**, **not iterable**, and does **not track size**
---

### 🔍 Side‑by‑Side Summary

| Feature | Map | WeakMap |
|--------|------|----------|
|created|new Map()|new WeakMap()|
| **Key Types** | Any type (objects, primitives, functions) | Objects only |
| **Memory Behavior** | Keys persist until removed | Keys removed automatically when unreferenced |
| **Iteration** | Fully iterable | Not iterable |
| **Size Tracking** | Has `size` | No `size` |
| **Use Case** | General key‑value storage | Private data tied to object lifetimes |
|**Methods**|`set(key, value)`, `get(key)`, `has(key)`, `delete(key)`, `clear(all key/value)`, `entries(check)`, `forEach()`, `size` |`set()`, `get()`, `has()`, `delete()`|
|Take the Map -> Map.get(objectKey)|change its values| nameRetrievedObj.nameoOjProperty = propertyValue;|
|**Core Idea**|Use a **Map** for flexibility and iteration. |Use a **WeakMap** for memory‑safety, object‑bound data that disappears|
---

## JavaScript Maps, Sets, WeakSets, and WeakMaps — What They Are, How They’re Created, and How They Differ

| Structure | What it **is** | How it’s **created** (examples from your paragraph) | What it **stores** | Key behaviors | Iterability | Memory behavior |
|----------|-----------------|-------------------------------------------------------|---------------------|----------------|--------------|------------------|
| **Set()** | manages a **collection of unique values** | `const set = new Set([1, 2, 3, 4, 5]);` | Primitives or objects | `add`, `delete`, `has`, `clear`, `size`, `forEach`; insertion order preserved | Fully iterable (`for…of`, `keys`, `values`) | Strong references (values stay until removed) |
| **WeakSet** | A collection of **weakly held object references** |`const ws = new WeakSet([obj1, obj2]);` | **Only objects** | `add`, `delete`, `has`; no `clear` or iteration | **Not iterable** | Weak references (objects removed automatically when unreferenced) |
| **Map** | A built‑in object that holds **key–value pairs**, like an object but more flexible | `const map = new Map([ ['flower', 'rose'], ['fruit', 'apple'], ['vegetable', 'carrot'] ]);` | Keys of any type; values of any type | `set`, `get`, `delete`, `has`, `clear`, `forEach`; ordered keys | Fully iterable (`keys`, `values`, `entries`) | Strong references (keys stay until removed) |
| **WeakMap** | A collection of **key–value pairs with weak object keys** | `const wm = new WeakMap([[objKey, value]]);` | Keys must be **objects**; values any type | `set`, `get`, `delete`, `has`, `size`; no `clear` or iteration | **Not iterable** | Weak references (keys removed automatically when unreferenced) |

---


