
### 1. **Question: SQL-to-JSON Transformation**
You are given a list of rows from an SQL database represented as a list of dictionaries, where each dictionary corresponds to a row. Each row contains `user_id`, `name`, `age`, and `city`.

Write a Python function `transform_data(rows: List[Dict[str, Union[str, int]]]) -> Dict[int, Dict[str, Union[str, int]]]` that transforms the data into a dictionary format where the keys are the `user_id` values, and the corresponding value is a dictionary of the remaining fields (`name`, `age`, `city`).

#### Example:
```python
rows = [
    {"user_id": 1, "name": "Alice", "age": 25, "city": "New York"},
    {"user_id": 2, "name": "Bob", "age": 30, "city": "San Francisco"}
]
```
#### Output:
```python
{
    1: {"name": "Alice", "age": 25, "city": "New York"},
    2: {"name": "Bob", "age": 30, "city": "San Francisco"}
}
```

---

### 2. **Question: Process Log Files**
You are given a list of log file entries, where each entry is a string in the format `"[timestamp] user_id action"`. The `action` can be either `"start"` or `"stop"`. Your task is to write a Python function `process_logs(logs: List[str]) -> Dict[int, int]` that returns a dictionary mapping each `user_id` to the total duration (in seconds) they were active (i.e., between `start` and `stop`).

Assume:
- All `start` actions are followed by a `stop` for the same user.
- The `timestamp` is in the format `"YYYY-MM-DD HH:MM:SS"`.

#### Example:
```python
logs = [
    "[2024-01-01 10:00:00] 1 start",
    "[2024-01-01 10:05:00] 1 stop",
    "[2024-01-01 10:00:00] 2 start",
    "[2024-01-01 10:10:00] 2 stop"
]
```
#### Output:
```python
{
    1: 300,  # 5 minutes
    2: 600   # 10 minutes
}
```

---

### 3. **Question: Data Deduplication**
You are given a list of dictionaries representing records, where each dictionary contains `id`, `name`, and `email`. Write a Python function `deduplicate(records: List[Dict[str, str]]) -> List[Dict[str, str]]` that removes duplicate records based on the `email` field and returns a list of unique records. Keep the first occurrence of each email.

#### Example:
```python
records = [
    {"id": "1", "name": "Alice", "email": "alice@example.com"},
    {"id": "2", "name": "Bob", "email": "bob@example.com"},
    {"id": "3", "name": "Alice", "email": "alice@example.com"}
]
```
#### Output:
```python
[
    {"id": "1", "name": "Alice", "email": "alice@example.com"},
    {"id": "2", "name": "Bob", "email": "bob@example.com"}
]
```

---

### 4. **Question: Sliding Window Aggregation**
You are given a list of integers representing transaction amounts and a window size `k`. Write a Python function `sliding_window_sum(transactions: List[int], k: int) -> List[int]` that returns a list containing the sum of every sliding window of size `k`.

#### Example:
```python
transactions = [10, 20, 30, 40, 50]
k = 3
```
#### Output:
```python
[60, 90, 120]
```
#### Explanation:
- Sum of the first 3 transactions: `10 + 20 + 30 = 60`
- Sum of the next 3 transactions: `20 + 30 + 40 = 90`
- Sum of the last 3 transactions: `30 + 40 + 50 = 120`

---

### 5. **Question: Flatten Nested JSON**
You are given a nested JSON-like dictionary structure. Write a Python function `flatten_json(nested_dict: Dict[str, Any]) -> Dict[str, Any]` that flattens the dictionary, where nested keys are represented as a concatenation of keys separated by a period (`.`).

#### Example:
```python
nested_dict = {
    "user": {
        "id": 1,
        "details": {
            "name": "Alice",
            "address": {
                "city": "New York",
                "zipcode": 10001
            }
        }
    }
}
```
#### Output:
```python
{
    "user.id": 1,
    "user.details.name": "Alice",
    "user.details.address.city": "New York",
    "user.details.address.zipcode": 10001
}
```

### 6. **Question: Find Top N Frequent Words**
You are given a list of words, and you need to find the top N most frequent words. Write a Python function `top_n_frequent_words(words: List[str], n: int) -> List[str]` that returns a list of the top N frequent words. The result should be sorted by frequency, and if two words have the same frequency, they should be sorted lexicographically.

#### Example:
```python
words = ["apple", "banana", "apple", "orange", "banana", "apple"]
n = 2
```
#### Output:
```python
["apple", "banana"]
```

---

### 7. **Question: Merge DataFrames**
You are given two lists of dictionaries, `employees` and `departments`, which represent two tables in a relational database. Each employee has a `department_id` that links them to a department. Write a Python function `merge_data(employees: List[Dict[str, Union[str, int]]], departments: List[Dict[str, str]]) -> List[Dict[str, Union[str, int]]]` that merges the two datasets into one, adding the `department_name` to each employee's data.

#### Example:
```python
employees = [
    {"id": 1, "name": "Alice", "department_id": 2},
    {"id": 2, "name": "Bob", "department_id": 1}
]
departments = [
    {"id": 1, "department_name": "Engineering"},
    {"id": 2, "department_name": "Marketing"}
]
```
#### Output:
```python
[
    {"id": 1, "name": "Alice", "department_id": 2, "department_name": "Marketing"},
    {"id": 2, "name": "Bob", "department_id": 1, "department_name": "Engineering"}
]
```

---

### 8. **Question: Moving Average of a Data Stream**
Write a class `MovingAverage` that computes the moving average of the last `k` values from a data stream. The class should implement two methods:
- `__init__(self, k: int)` initializes the moving average with the window size `k`.
- `next(self, val: int) -> float` returns the moving average of the last `k` values.

#### Example:
```python
ma = MovingAverage(3)
print(ma.next(10))  # returns 10.0
print(ma.next(20))  # returns 15.0
print(ma.next(30))  # returns 20.0
print(ma.next(40))  # returns 30.0
```

#### Explanation:
- After the first value (10), the average is 10.
- After the second value (20), the average of [10, 20] is 15.
- After the third value (30), the average of [10, 20, 30] is 20.
- After the fourth value (40), the window shifts to [20, 30, 40], and the average is 30.

---

### 9. **Question: JSON Field Renaming**
You are given a list of dictionaries representing JSON objects, where each dictionary has fields `name`, `age`, and `location`. Your task is to write a Python function `rename_fields(data: List[Dict[str, Union[str, int]]]) -> List[Dict[str, Union[str, int]]]` that renames the field `location` to `city` for each dictionary in the list.

#### Example:
```python
data = [
    {"name": "Alice", "age": 25, "location": "New York"},
    {"name": "Bob", "age": 30, "location": "San Francisco"}
]
```
#### Output:
```python
[
    {"name": "Alice", "age": 25, "city": "New York"},
    {"name": "Bob", "age": 30, "city": "San Francisco"}
]
```

---

### 10. **Question: Reformat Date Strings**
You are given a list of date strings in the format `"DD-MM-YYYY"`. Write a Python function `reformat_dates(dates: List[str]) -> List[str]` that reformats each date into the format `"YYYY-MM-DD"`.

#### Example:
```python
dates = ["31-12-2024", "01-01-2024"]
```
#### Output:
```python
["2024-12-31", "2024-01-01"]
```


