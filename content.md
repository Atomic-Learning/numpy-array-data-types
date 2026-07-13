# Python: NumPy Array Data Types

NumPy arrays are required to store values with a single common type. When you mix values of different types, NumPy converts them so all entries have the same type where possible.

```py-cell
import numpy as np

string_array = np.array(["str1", "str2"])
print(string_array)

bool_array = np.array([True, False])
print(bool_array)
```

If the values have different types, NumPy chooses a common type for the array.

```py-cell
import numpy as np

mixed_array = np.array([1, 1.2])
print(mixed_array)

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
