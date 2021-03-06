# Functions

{{ stub }}

- def print_addition(a, b): print(a + b);
- Double-column and indentation as code blocks
- Good practice: be coherent in the number of spaces. A common practice is to use four spaces, this is the default in Spyder.
- List of arguments: print_addition(2, 4)
- Keyword arguments: print_addition(a=2, b=4)
    - Coding style: note the absence of space between variable name and value (PEP8).
- Default values: def print_addition(a, b, c=0): print(a + b + c);
    - print_addition(2, 4)
    - print_addition(2, 4, 6)
    - print_addition(a=2, b=4, c=6)
- Returning values
    - def print_addition(a, b, c=0): total = a + b + c; return total;
    - print(print_addition(2, 4, 6))
- Good practice in naming functions: active form and lowercase with underscores (PEP8).
- Good practice with Docstrings
    - Docstring for each function. Very important. PEP8: First line is verb to period. The rest is a detailed description if required.
- Integration exercise: speed calculation
    - Program a function that will make this code work as expected:
    - print(calculate_speed(0.0, 5.4, 50.0))
    - print(calculate_speed(time_gate1=0.0, time_gate2=5.4, distances_gates12=50.0))
