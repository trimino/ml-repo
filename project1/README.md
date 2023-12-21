# Assignment 1

## Task 1

```python=
def factorial(n):
    result = 1
    for i in range(2, (n+1)):
        result = result * i
    return result
```

Consider the factorial function above, implemented in Python. What is the time complexity of this function, in Θ notation, with respect to n?

## Task 2

Re-implement, in Python, the factorial function of *Task 1* so that it uses a **recursive function call** instead of using any loops (like while loops and for loops). Do not call any built-in or library functions for computing the factorial. You do NOT need to do any error-checking (like checking if the input argument is negative). For this task, please include your code in the answers.pdf file, do NOT submit a separate code file.

## Task 3

```python=
def foo(n):
    result = 0
    for i in range(1, (n+1)):
        for j in range(1, (i+1)):
            result = result + 1
    return result
```

Consider the foo function above, implemented in Python. What is the time complexity of this function, in Θ notation?

## Task 4

Consider matrices A and B defined as:

```math
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
, 
B = \begin{bmatrix}
e \\\
f
\end{bmatrix}
```

What is the result of matrix multiplication A*B? Specify the values at all positions of the result matrix, in terms of the symbols a, b, c, d, e, f.

## Task 5

Consider function $$f(x)= 3x^2 + 5x - 7$$

**Part a:** What is the first derivative f'(x)? Provide a specific formula as a function of x.

**Part b:** What is f'(5)? Your answer should be a real number.

**Part c:** What is the second derivative f''(x)? Provide a specific formula as a function of x.

**Part d:** What is f''(5)? Your answer should be a real number.

## Task 6

Consider function $$f(x, y) = 3x^2y + 5x - 7y$$

**Part a:** What is the partial derivative of f with respect to x? Provide a specific formula as a function of x and y.

**Part b:** What is the partial derivative of f with respect to x when x=5 and y=2? Your answer should be a real number.

## Task 7

In this task, we denote by P(x) the probability of event x. A and B are two events that are independent of each other. P(A) = 0.3 and P(B) = 0.6.

Compute the following quantities:

* P(A and B).
* P(A or B).
* P(not(A)).
* P(A | B) (i.e., the conditional probability of A given B).

## Task 8

| Color | Price $20 to $40 | Price $50 to $70 | Price $80 to $100 |
| :---------: | :---------: | :---------: | :---------: |
| red | 40 | 70 | 35 |
| green | 15 | 50 | 30 |
| blue | 60 | 20 | 80 |

The above table shows, for a certain hat store, the number of hats in their inventory, for each combination of color and price. For example, the inventory contains 40 red hats at a price between $20 and $40. Using that table:

**Part a:** Determine P(price < $75), i.e., the probability that a hat costs less than $75.

**Part b:** Determine P(price < $75 | color=green), i.e., the conditional probability that the price of a hat is under $75, given that the color of that hat is green.

**Part c:** Determine P(price < 75, color=green), i.e., the joint probability that the price of a hat is under 75 and the color of that hat is green.

## Task 9

Two hens lay a combined total of two eggs in two days. If this rate of egg production per hen per day continues, how many eggs do ten hens lay in ten days?

## Task 10

Implement a a Python executable file called **file_stats.py** that reads computes the average and standard deviation of each column of numbers contained in some specified file. In particular, your program should be invoked from the command line as follows:
> python file_stats.py pathname

**Argument "*pathname*" is the path name of the data file.** The path name can specify any file stored on the local computer (not just in the current directory). This file will contain data in tabular format, so that each value is a number, and values are separated by white space. An example of such a file is [numbers1.txt](./numbers1.txt).

Returns the average and standard deviation of the numbers contained in the file. For standard deviation, please use the formula that divides by n-1 (when we have n numbers in our dataset). You can assume that the dataset will contain at least two rows, and each all rows contain the same number of values. The program should print a line for each column of the data, and that line should follow this format:

> Column %d: mean = %.4f, std = %.4f

For example, if [numbers1.txt](./numbers1.txt) is the input file, the output should look exactly like this:
> Column 1: mean = 62.3855, std = 34.5852
Column 2: mean = 66.0211, std = 33.0843
Column 3: mean = 58.7307, std = 29.3490
Column 4: mean = 39.7816, std = 36.0666
Column 5: mean = 56.1361, std = 20.2483

Please place your python code in a file called file_stats.py.

## Task 11

Write a python function
> result = nth_smallest(data, top, bottom, left, right, n)

with these specs:

* The first argument, data, is a two-dimensional numpy array.
* The function returns the n-th smallest value in the subarray of data that goes from row top up to (and including) row bottom, and from column left up to (and including) column right.

For example, consider this code:

```python=
import numpy as np

def nth_smallest(data, top, bottom, left, right, n):
# your code goes here

a = np.array([[0.8147, 0.0975, 0.1576, 0.1419, 0.6557, 0.7577],
       [0.9058, 0.2785, 0.9706, 0.4212, 0.4212, 0.7431],
       [0.127 , 0.5469, 0.9572, 0.9157, 0.8491, 0.3922],
       [0.9134, 0.9575, 0.4854, 0.7922, 0.934 , 0.6555],
       [0.6324, 0.9649, 0.8003, 0.9595, 0.6787, 0.1712]])

print(nth_smallest(a, 1, 2, 3, 4, 1))
print(nth_smallest(a, 1, 2, 3, 4, 2))
print(nth_smallest(a, 1, 2, 3, 4, 3))
print(nth_smallest(a, 1, 2, 3, 4, 4))
```

If you implement the *nth_smallest function* correctly, the above code should print:

```bash=
0.4212
0.4212
0.8491
0.9157
```

Please place your python code in a file called *nth_smallest.py*
