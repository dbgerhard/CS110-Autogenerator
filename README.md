
# Autogenerated Questions for CS110


This is a collection of random, autogenerated multiple choice questions for the use of CS110 quizzes.
By inputting the options outlined in control.txt and running Source.cpp, a .txt file is created containing the specified questions in GIFT format.

Here is each category of questions with examples of each difficulty (or subcategory) listed by Roman numerals. The correct answers are in bold.

## Arrays

##### (i) - Element Swap
What are the contents of the array after the following statements?
```cpp
int bar[6] = {6, 5, 3, 8, 1, 9};
int temp;
temp = bar[4];
bar[4] = bar[1];
bar[1] = temp;
```

- **```{6, 1, 3, 8, 5, 9}```**
- ```{6, 5, 3, 8, 1, 9}```
- ```{8, 5, 3, 8, 1, 3}```
- ```{8, 5, 3, 6, 1, 9}```
- ```{6, 5, 9, 8, 1, 3}```


##### (ii) - Element access
What are the contents of a given array after all elements are incremented by 1, 5, or 10.
```cpp
int foo[5] = {4, 0, 7, 1, 5};
for (int i = 0; i < 5; i += 1)
{
	foo[i] += 10;
}
```
- **```{14, 10, 17, 11, 15}```**
- ```{15, 11, 18, 12, 1}```
- ```{0, 1, 2, 3, 4}```
- ```{-6, -10, -3, -9, -5}```
- ```{4, 0, 7, 1, 5}```


##### (iii) - Incorrect element access
What is printed after the following statements?
There is an option for out of bounds indexing (hence the last distractor may be correct at times).
```cpp
int list[6] = {5, 10, 4, 1, 3, 7};
for (int i = 1; i < 5; i = i + 2)
{
	cout << list[i] << " ";
}
```
- **10 1**
- 1 7
- 1 10
- 5 4
- Run-time error due to out of bound index.


## Loops

All Loops have the same nature of questions, they are just in different formats based on
selection (For Loop, While Loop, or Do While Loop). Each also has the option of "improper"
loops, meaning that the loop conditions are such that the statement will execute billions
of times (due to integer overflow).

Here are all of the currently used Loop questions.

### Loop Counting

##### (i) - Single Loops using additive updates

How many times does the '\*' print?
```cpp
for (int i = 10; i < 25; i = i + 5)
{
	cout << '\*';
}
```
- **3**
- 2
- 4
- 0
- 1

##### (ii) - Single Loops using additive and subtractive updates with improper loops

How many times does the '\*' print?
```cpp
int c = 44;
do
{
	cout << '\*';
	c = c - 5;
} while (c > 24);
```
- **4**
- 3
- 5
- 0
- Around a couple billion


##### (iii) - A similar question to (ii) but multiplicative and divisive (?) updates

How many times does the '\*' print?
```cpp
int a = 1;
while (a < 189)
{
	cout << '\*';
	a \*= 10;
}
```
- **3**
- 2
- 4
- 0
- Around a couple billion


##### (iv) - A similar question to (ii) but with nested loops

How many times does the '\*' print?
```cpp
for (int i = 90; i > 60; i = i - 10)
{
	for (int j = 30; j < 62; j = j + 10)
	{
		cout << '\*';
	}
}
```
- **12**
- 4
- 3
- 11
- 16


### Loop Printing

This is currently only used for single loops in (i) - (iii). I think this would be too difficult with nested loops.

##### (i) - Single Loops that output the "loop variable" at every iteration

What is the following output of the code?
```cpp
int g = 6;
while (g < 10)
{
	cout << g << ' ';
	g += 1;
}
```
- **6 7 8 9**
- 7 8 9
- 7 8 9 10
- 6 7 8
- 6 7 8 9 10

##### (ii) Similar to (i) but with subtraction as well

What is the following output of the code?
```cpp
int b = 61;
do
{
	cout << b << ' ';
	b = b - 10;
} while (b > 20);
```
- **61 51 41 31 21**
- 51 41 31 21
- 51 41 31 21 11
- 61 51 41 31
- 61 51 41 31 21 11

##### (iii) Similar to (ii) but with multiplicative and divisive increments

What is the following output of the code?
```cpp
for (int c = 21; c > 4; c = c / 2)
{
	cout << c << ' ';
}
```
- **21 10 5**
- 10 5
- 10 5 2
- 21 10
- 21 10 5 2


## Expressions

##### (i) - (iv) Integer Expressions
 All subcategories are the same, but with different number of operands.

Solve the following problem:
```cpp
int foo = 2;
int bar = foo * 4 % 2 + 4;
```
What is the variable "bar" equal to?

- **4**
- 5
- 5.5
- 6
- 8

## Functions

##### (i) - Reference Parameters
The order of the parameters and the arguments have the option of being randomized.

Given the following function definition:
```cpp
void Calculate(int& a, int& b, int c)
{
	b = a / b + c;
}
```
What value is printed after the following statments?
```cpp
int marks = 5;
int matrix = 4;
int item = 5;
Calculate(marks, matrix, item);
cout << matrix << endl;
```

- **6**
- 4
- 3
- 5
- 1

##### (ii) - Parameter data types
The return type is always float to give the most general return value.

Given the following function definition:
```cpp
float Switch(float a, int b)
{
    return a - b;
}
```
What is printed from the following call?
```cpp
cout << Switch(3.5, 1.5) << endl;
```

- **2.5**
- -1
- 4.5
- -2.5
- 2


##### (ii) - Function return types
The main random element is the function return type, which forces type coercion. There is also a possibility that the return type is void, and the correct answer is "Compile-time Error".

Given the following function definition:
```cpp
int Pow()
{
	return 4.5 + 1.0;
}
```
What is printed from the following call?
```cpp
cout << Pow() << endl;
```

- **5**
- 6.5
- 5.5
- Run-time error.
- Compile-time error.


## Switch Cases

##### (i) - A switch case statement with random breaks and possibly a default case.

What is the value of bar after the switch/case block?
```cpp
int bar = 4;
switch (bar) {
	case 2:
		bar = 5;
		break;
	case 4:
		bar = 6;
		break;
	case 1:
		bar = 4;
	case 3:
		bar = 0;
	case 0:
		bar = 1;
		break;
}
```
- **6**
- 8
- 5
- 4
- 1

##### (ii) - A "normal" switch case statement with all breaks and always a default case.

What is the value of list after the switch/case block?
```cpp
int list = 4;
switch (list) {
	case 3:
		list = 3;
		break;
	case 0:
		list = 2;
		break;
	case 2:
		list = 0;
		break;
	default:
		list = 1;
}
```
- **1**
- 0
- 2
- 4
- 3


##### (iii) - A switch case statement with no breaks, but with a default.

What is the value of item after the switch/case block?
```cpp
int item = 3;
switch (item) {
	case 2:
		item = 4;
	case 3:
		item = 0;
	case 4:
		item = 3;
	case 5:
		item = 1;
	default:
		item = 6;
}
```
- **6**
- 0
- 2
- 3
- 8

##### (iv) - A switch case statement with no breaks and no default.

What is the value of item after the switch/case block?
```cpp
int item = 3;
switch (item) {
	case 6:
		item = 1;
	case 0:
		item = 0;
	case 5:
		item = 2;
	case 4:
		item = 4;
	case 2:
		item = 5;
}
```
- **3**
- 1
- 6
- 4
- 5


## Identifiers

##### (i) - (iv) A randomly generated string with a chance of starting with a number, or having invalid characters

Is the following a valid C++ identifier?
```Tb306wN```

- **True**
- False


## Conditionals

##### (i) A logical expression comparing two other logical expressions

What is the result of the following logical expression?
```cpp
int numbers = 3;
int marks = 8;
(numbers >= 4) == (marks >= 10)
```
- **True**
- False

##### (ii) The same question as (i) but with 3 different logical subexpressions

What is the result of the following logical expression?
```cpp
int documents = 7;
int standings = 6;
int matrix = 5;
(documents > 1) == (standings > 5) || (matrix > 1)
```
- **True**
- False

##### (iii) The same as (i) but with a random order of operands
What is the result of the following logical expression?
```cpp
int documents = 8;
int bar = 10;
(bar <= documents) != (10 < 9)
```
- **False**
- True

##### (iv) The same as (ii) but with a random order
What is the result of the following logical expression?
```cpp
int bar = 6;
int marks = 7;
int matrix = 3;
(marks >= matrix) || (bar < 8) && (1 < 2)
```
- **True**
- False
