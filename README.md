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
| **Key Types** | Any type (objects, primitives, functions) | Objects only |
| **Memory Behavior** | Keys persist until removed | Keys removed automatically when unreferenced |
| **Iteration** | Fully iterable | Not iterable |
| **Size Tracking** | Has `size` | No `size` |
| **Use Case** | General key‑value storage | Private data tied to object lifetimes |
|**Methods**|`set()`, `get()`, `has()`, `delete()`, `clear()`, `entries()`, `forEach()` |`set()`, `get()`, `has()`, `delete()`|
---
### 🧠 Core Idea  
Use a **Map** when you need flexibility and iteration.  
Use a **WeakMap** when you want memory‑safe, object‑bound data that disappears automatically.

