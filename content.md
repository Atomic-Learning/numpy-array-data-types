A single NumPy arrays always stores values of a single common type. NumPy arrays are capable of storing values of many different types, including:

```py-cell
import numpy as np

# An array of integers
int_array = np.array([1, 2, 3])
print(int_array)

# An array of floats
float_array = np.array([1.0, 2.0, 3.0])
print(float_array)

# An array of strings
string_array = np.array(["str1", "str2"])
print(string_array)

# An array of booleans
bool_array = np.array([True, False])
print(bool_array)
```
When you mix values of different types, NumPy converts them so all entries have the same type where possible:

```py-cell
import numpy as np

# The integer 1 is converted to a float so that all values are floats.
mixed_array = np.array([1, 1.2])
print(mixed_array)

# The integer 4 is converted to a string so that all values are strings.
mixed_array2 = np.array([4, "str"])
print(mixed_array2)
```

You can inspect the stored data type with the `dtype` property.

```py-cell
import numpy as np

array1 = np.array([1, 2])
print(array1.dtype)

array2 = np.array([True, False])
print(array2.dtype)

array3 = np.array(["1", "2"])
print(array3.dtype)

array4 = np.array(["1234567890", "2"])
print(array4.dtype)

array5 = np.array([1.0, -2.0])
print(array5.dtype)
```

These dtypes are NumPy's internal storage types rather than the usual high-level Python types. They let NumPy store and process array data efficiently.
