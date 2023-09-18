# Homework 2 - Functions
- Due date and submission details to be determined. 
- If you have questions, [post them to the Issue Tracker](https://github.com/IE-555/fall2023/issues/4).  Emailed questions will not be answered.

--- 

In this assignment you are asked to submit a single file, named `myFunctions.py` which will contain several functions as described below.

--- 

1. Write a function named `describe_that_int` that takes an integer value and returns a string 'even' if the input is an even number, or returns 'odd' if the input is an odd number.  Your function will **only** be given an integer as an input (i.e., you do not need to worry about a user passing a string, a float, a list, etc. to your function).

2. Write a function named `my_extreme_values` that takes a Python list as an input.  The function should return a tuple, of the form `(minimum value, maximum value)`, which contains the minimum and maximum numeric values in the list.

    - NOTE:  The list might contain non-numeric values, which your function should ignore.  In such a case, let the minimum value be `float('inf')` and the maximum value be `-float('inf')`.  Some examples:

        ```
        import myFunctions
        
        myFunctions.my_extreme_values([1, 99, -3]) 
        # would return (-3, 99)
        
        myFunctions.my_extreme_values(['hi', 207, 5, '1000']) 
        # would return (5, 207)
        
        myFunctions.my_extreme_values(['hi', '1000', 123]) 
        # would return (123, 123)
        
        myFunctions.my_extreme_values(['hi', '1000']) 
        # would return (float('inf'), -float('inf'))
        ```


3. Write a function that will take as an input a single Python list.  Your function, which should be named `multiply_by_two`, should return a list that contains all of the values in the input list multiplied by two (2).  You may assume that the input list will only contain numeric values (integers and/or floats).  Be careful that your function does not modify any variables **outside** of the function.  For example:

    ```
    import myFunctions
    
    a = [1, 2, 3]
    c = myFunctions.multiply_by_two(a)
    
    print(c)   # This should be [2, 4, 6]
    print(a)   # Make sure this is [1, 2, 3].  
    ```


4. Write a function named `count_the_elements` that will return the total number of elements in a given list.  For example:
    - `['abcde']`` has 1 element
    - `[1.2, 3.4, -5.6]` has 3 elements
    - `[1, 2, [3]]` has 3 elements
    - `[1, [2, 5.2], -7.9, [3, [-2, 3.]]]` has 7 elements
    - `['abc', ['d', [5]]]` has 3 elements



5. Write a function, of the form `exclusion(a, b)`, that returns a Python **set** containing all of the elements that are in `a` but are not in `b`.  `a` and `b` can be sets, lists, or tuples, although they will not be nested (i.e., `[1, 2, 3]`, `{1, 2, 3}`, and `(1, 2, 3)` would be valid inputs; `[1, [2, 3]]` is nested and would not be passed as an input to your function).



6. Write a function that will accept two inputs, in this order:  
    1. A list of animal names;
    2. A list of colors.

    Your function should be named `animalColors`.  It will return a dictionary, where each animal name is a key and each color is the value associated with the corresponding animal name.  Both input lists will be of the same length.  An example:

    ```
    import myFunctions

    myFunctions.animalColors(['lion', 'tiger'], ['red', 'yellow'])
    # would return `{'lion': 'red', 'tiger': 'yellow'}`
    ```

7. Write a function named `ceiling_plus_1` that will accept a scalar numeric value as an input.  It should return the ceiling of that number plus one (1).  For example:

    ```
    import myFunctions

    myFunctions.ceiling_plus_1(7.2)
    # would return 9
    ```
    You may assume that the user would never try to pass anything to your function besides a scalar numeric value.


8. Write a function that will return a given floating point value as a string representing the input value as a US dollar, rounded to exactly two (2) decimal places.  The dollar sign (`$`) should be the first character of the return string.  There should be no space between the `$` and the first digit (i.e., `$1.50` is correct; `$ 1.50` and `1.50$` are both incorrect).  Exactly two (2) decimal places should always be shown.

    The function should be named `dollar_string`.

    ```
    import myFunctions

    myFunctions.dollar_string(1.2)
    # should return the string '$1.20'

    myFunctions.dollar_string(1/3)
    # Should return the string '$0.33'

    myFunctions.dollar_string(4/2)
    # Should return the string '$2.00'

    myFunctions.dollar_string(2/4)
    # Should return the string '$0.50'
    ```

    NOTE: The input is a scalar float; the output is a string.





10. Write a function of the form `find_these(a, b, c)`, such that 
    - `a` is a scalar value (it could be an `int`, a `float`, or a `string`);
    - `b` is a dictionary; and 
    - `c` is a list, a set, or a tuple.

    The function should return a tuple of the form `(d, e)`, where `d` is `True` if `a` is a value in `b` (`False` otherwise) and `e` is `True` if `a` is a value in `c` (`False` otherwise).

11. Write a function named `multiply_by_four`.  Similar to the `multiply_by_two` function, the output should be a list that contains all of the input values multiplied by a number (this time, that number is four (4)).  However, in this function, the user can pass nested Python lists.  For example, these would be valid inputs to your function:
    - `[1.2, 3.4, -5.6]`
    - `[1, 2, [3]]`
    - `[1, [2, 5.2], -7.9, [3, [-2, 3.]]]`



