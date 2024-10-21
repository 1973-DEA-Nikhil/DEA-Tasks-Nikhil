### Question 1: Array Manipulation
**Problem Statement:**
Given a list of numbers, write a function that converts the list to a NumPy array, reshapes it into a 2D array with a specified number of columns, and returns the reshaped array.

**Function Signature:**
```python
def reshape_array(data: List[float], num_columns: int) -> np.ndarray:
```

---

### Question 2: Statistical Analysis
**Problem Statement:**
Write a function that takes a NumPy array of numerical data and returns a dictionary containing the mean, median, standard deviation, and variance of the array.

**Function Signature:**
```python
def calculate_statistics(data: np.ndarray) -> Dict[str, float]:
```

---

### Question 3: Element-wise Operations
**Problem Statement:**
Create a function that takes two NumPy arrays of the same shape and returns a new array that contains the element-wise product of the two arrays. Handle cases where the arrays may contain zeros.

**Function Signature:**
```python
def elementwise_product(arr1: np.ndarray, arr2: np.ndarray) -> np.ndarray:
```

---

### Question 4: Masking and Filtering
**Problem Statement:**
Given a NumPy array of integers, write a function that returns a new array containing only the even numbers from the original array. Use NumPy’s masking capabilities to achieve this.

**Function Signature:**
```python
def filter_even_numbers(data: np.ndarray) -> np.ndarray:
```

---

### Question 5: Dot Product and Matrix Multiplication
**Problem Statement:**
Write a function that takes two 2D NumPy arrays (matrices) and computes their dot product. Ensure that the function checks the dimensions of the matrices to confirm that the dot product can be performed.

**Function Signature:**
```python
def matrix_dot_product(mat1: np.ndarray, mat2: np.ndarray) -> np.ndarray:
```

---
### Question 6: Concatenation of Arrays
**Problem Statement:**
Write a function that takes a list of NumPy arrays and concatenates them along a specified axis. Return the resulting concatenated array.

**Function Signature:**
```python
def concatenate_arrays(arrays: List[np.ndarray], axis: int) -> np.ndarray:
```

---

### Question 7: Sorting and Indexing
**Problem Statement:**
Given a NumPy array of integers, write a function that returns a sorted version of the array along with the indices that would sort the array.

**Function Signature:**
```python
def sort_array_and_indices(data: np.ndarray) -> Tuple[np.ndarray, np.ndarray]:
```

---

### Question 8: Reshaping and Transposing
**Problem Statement:**
Write a function that takes a 1D NumPy array and reshapes it into a 3D array with specified dimensions. If the reshape is not possible, the function should raise a ValueError. Then, return the transposed version of the 3D array.

**Function Signature:**
```python
def reshape_and_transpose(data: np.ndarray, shape: Tuple[int, int, int]) -> np.ndarray:
```

---

### Question 9: Unique Values and Counts
**Problem Statement:**
Write a function that takes a NumPy array and returns two arrays: one containing the unique values in the original array and another containing the counts of those unique values.

**Function Signature:**
```python
def unique_values_and_counts(data: np.ndarray) -> Tuple[np.ndarray, np.ndarray]:
```

---

### Question 10: Broadcasting
**Problem Statement:**
Given a 2D NumPy array and a 1D NumPy array, write a function that adds the 1D array to each row of the 2D array using NumPy's broadcasting feature. Return the resulting array.

**Function Signature:**
```python
def add_with_broadcasting(matrix: np.ndarray, vector: np.ndarray) -> np.ndarray:
```

