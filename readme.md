# Difference Between `is` and `in` in Python


1. `is` Operator

The `is` operator is used to compare the identity of two objects. It checks whether two variables point to the same object in memory, not whether their values are equal.

Syntax:
a is b

Explanation:
When you use `is`, you’re asking: “Are these two variables referencing the exact same object?”

Example:
x = [1, 2, 3]
y = x
z = [1, 2, 3]

print(x is y)  # True, because y references the same object as x
print(x is z)  # False, because z is a separate object with the same contents

When to Use:
Identity checks, especially for singleton objects like None:
if value is None:
    # Do something

2. `in` Operator

The `in` operator is used to check membership. It tests whether a value exists inside an iterable (like a list, tuple, string, set, or dictionary keys).

Syntax:
element in container

Explanation:
When you use `in`, you're asking: “Does this element exist inside this container?”

Example:
my_list = [10, 20, 30]

print(20 in my_list)   # True, because 20 is in the list
print(40 in my_list)   # False, 40 is not in the list

text = "python"
print("p" in text)     # True
print("z" in text)     # False
