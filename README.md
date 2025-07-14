# Dictionary:

---

**Defination:**
-A *Dictionary* in Python is a collection of key-value pairs used to store data. It is unordered, mutable, and indexed by keys.

**Basic example:**
```python
student = {
    "name": "Pavani",
    "age": 21,
    "course": "Python"
}
```
* name, age, course → keys

* "Pavani", 21, "Python" → values
  
**Dictionary Syntax:**
```python
dict_name = {
    key1: value1,
    key2: value2,
    ...
}
```
* Keys and values are separated by a colon :

* Each pair is separated by a comma ,

**Key-Value Pair Rules:**
```

🔷 Keys:
```
* Must be unique

* Must be immutable (not changeable)

* ✅ Valid types: int, float, str, bool, tuple

* ❌ Invalid types: list, dict, set (because they are mutable)

```
🔷 Values:
```
* Can be any type: string, number, list, tuple, dictionary, etc.

* Can be duplicated
```
✅ Examples of Valid Keys and Values:
```
* All key types are valid:
```python
my_dict = {
    "name": "Pavani",        # str key -> str value
    101: "roll number",      # int key -> str value
    (1, 2): [10, 20],        # tuple key -> list value
    True: "Yes",             # bool key -> str value
    "marks": [90, 95, 88],   # str key -> list value
    "details": {"city": "Hyd"}  # nested dictionary
}
```
```
❌ Invalid Key Example (causes error):
```
* list cannot be a key:
```python
invalid_dict = {
    [1, 2]: "not allowed"  # ❌ Error: unhashable type: 'list'
}
```
✅ Accessing Dictionary Values:

1. Using Square Brackets (raises error if key not found):

```python
print(my_dict["name"])  * Pavani
```
2. Using .get() method (safe way):

```python
print(my_dict.get("marks"))        # [90, 95, 88]
print(my_dict.get("grade", "N/A")) # N/A (default if not found)
```
✅ Looping through a Dictionary:

🔹 Loop through keys:
```python
for key in my_dict:
    print(key)
```
🔹 Loop through values:
```python
for value in my_dict.values():
    print(value)
```
🔹 Loop through key-value pairs:
```python
for key, value in my_dict.items():
    print(key, ":", value)
```
🧪 Example Program: Student Info:
```python
student = {
    "name": "Charan",
    "age": 22,
    "skills": ["Python", "SQL"],
    "score": 88.5,
    "details": {"city": "Hyderabad", "pincode": 500001}
}

* Access:
print("Name:", student["name"])
print("City:", student["details"]["city"])

* Loop through key-value pairs:
for k, v in student.items():
    print(f"{k} => {v}")
```
