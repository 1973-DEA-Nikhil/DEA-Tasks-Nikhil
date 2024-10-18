### 1. **Question: CSV to Dictionary Conversion**
You are given a list of strings representing rows from a CSV file, where each string contains values separated by commas. Write a Python function `csv_to_dict(csv_rows: List[str]) -> List[Dict[str, str]]` that converts these rows into a list of dictionaries, using the first row as the header.

#### Example:
```python
csv_rows = [
    "id,name,age,city",
    "1,Alice,25,New York",
    "2,Bob,30,San Francisco"
]
```
#### Output:
```python
[
    {"id": "1", "name": "Alice", "age": "25", "city": "New York"},
    {"id": "2", "name": "Bob", "age": "30", "city": "San Francisco"}
]
```

---

### 2. **Question: Aggregate Sales Data**
You are given a list of sales records, where each record is a dictionary containing `product_id`, `quantity`, and `price`. Write a Python function `aggregate_sales(sales: List[Dict[str, Union[str, int]]]) -> Dict[str, float]` that returns a dictionary with the total revenue for each `product_id`.

#### Example:
```python
sales = [
    {"product_id": "A", "quantity": 2, "price": 10.0},
    {"product_id": "B", "quantity": 1, "price": 20.0},
    {"product_id": "A", "quantity": 1, "price": 10.0}
]
```
#### Output:
```python
{
    "A": 30.0,
    "B": 20.0
}
```

---

### 3. **Question: Date Range Filtering**
You are given a list of records, where each record is a dictionary with a `date` field in the format `"YYYY-MM-DD"`. Write a Python function `filter_by_date_range(records: List[Dict[str, str]], start_date: str, end_date: str) -> List[Dict[str, str]]` that returns a list of records whose dates fall within the specified range (inclusive).

#### Example:
```python
records = [
    {"date": "2024-01-01", "event": "New Year"},
    {"date": "2024-01-15", "event": "Meeting"},
    {"date": "2024-02-01", "event": "Conference"}
]
start_date = "2024-01-01"
end_date = "2024-01-31"
```
#### Output:
```python
[
    {"date": "2024-01-01", "event": "New Year"},
    {"date": "2024-01-15", "event": "Meeting"}
]
```

---

### 4. **Question: Calculate Mode of a List**
You are given a list of integers. Write a Python function `calculate_mode(numbers: List[int]) -> List[int]` that returns a list of the mode(s) of the list. If there are multiple modes, return them in ascending order.

#### Example:
```python
numbers = [1, 2, 3, 4, 4, 5, 5]
```
#### Output:
```python
[4, 5]
```

---

### 5. **Question: JSON Data Validation**
You are given a list of JSON objects where each object represents a user. Each user should have a `username` (string) and an `email` (string). Write a Python function `validate_users(users: List[Dict[str, str]]) -> List[str]` that returns a list of error messages for invalid users. An error message should specify whether the `username` or `email` is missing.

#### Example:
```python
users = [
    {"username": "Alice", "email": "alice@example.com"},
    {"username": "", "email": "bob@example.com"},
    {"email": "charlie@example.com"},
    {"username": "Dave"}
]
```
#### Output:
```python
[
    "Username is required for user with email bob@example.com",
    "Username is required for user with email charlie@example.com",
    "Email is required for user with username Dave"
]
```

---

### 6. **Question: JSON Deep Merge**
You are given two JSON-like dictionaries. Write a Python function `deep_merge(dict1: Dict[str, Any], dict2: Dict[str, Any]) -> Dict[str, Any]` that merges the two dictionaries. If both dictionaries have the same key, the value from `dict2` should overwrite the value from `dict1`. If the value is a dictionary, merge it recursively.

#### Example:
```python
dict1 = {"a": 1, "b": {"c": 2}}
dict2 = {"b": {"d": 3}, "e": 4}
```
#### Output:
```python
{
    "a": 1,
    "b": {"c": 2, "d": 3},
    "e": 4
}
```

---

### 7. **Question: Count Unique Values**
You are given a list of dictionaries representing items, where each dictionary has a `category` field. Write a Python function `count_unique_categories(items: List[Dict[str, str]]) -> int` that counts the number of unique categories present in the list.

#### Example:
```python
items = [
    {"name": "Item1", "category": "A"},
    {"name": "Item2", "category": "B"},
    {"name": "Item3", "category": "A"}
]
```
#### Output:
```python
2
```

---

### 8. **Question: Generate Fibonacci Series**
Write a Python function `fibonacci(n: int) -> List[int]` that returns the first `n` numbers of the Fibonacci series.

#### Example:
```python
n = 5
```
#### Output:
```python
[0, 1, 1, 2, 3]
```

---

### 9. **Question: Simple Calculator**
You are tasked with creating a simple calculator. Write a Python function `calculate(expression: str) -> float` that takes a string expression (e.g., `"3 + 5"`, `"10 - 2"`) and returns the result of the calculation.

#### Example:
```python
expression = "3 + 5"
```
#### Output:
```python
8.0
```

---

### 10. **Question: Normalize Text**
You are given a list of strings. Write a Python function `normalize_text(lines: List[str]) -> List[str]` that removes extra whitespace from each string and converts it to lowercase.

#### Example:
```python
lines = ["  Hello World  ", "Python  Programming   "]
```
#### Output:
```python
["hello world", "python programming"]
```

