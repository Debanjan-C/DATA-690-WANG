Debanjan Chowdhury
Data 690 - Stats and Viz

# Chapter 1 Notes

## Types of data used
1. We are mainly focusing on **structured data** for this chapter. Some examples are:
    - Tabular or Spreadsheet - Each column of the data may be of different types like
      numeric, date, string, etc. These are commonly found in relational databases or comma
      delimited files like CSV files.
    - Multidimensional arrays or matrices are a good example.
    - Multiple tables of with co-related data that is related through the primary key of one 
      table and the foreign key of another table.
    - Time series that are evenly or unevenly spaced out.
    - and there are many other examples.
    ....
 
## Python
1. First appearance was in 1991 and it was one of the most popular interpreted programming languages with Ruby, Perl and any others.
    - Since 2005, Python and Ruby have become a great option for developing websites using a number of 
      frameworks like Django for Python and Rails for Ruby.
    - These languages are called scripting languages as they can be used to write small programs or      scripts and use it to automate other tasks. 
2. Python is one of the most important languages for Data Science, Machine Learning and general Software Engineering in academia and many industries.
    - In terms of data analysis, interactive computing and data visualization, python has similarities with other programming languages like R, MATLAB, SAS, STATA and many others. 

## Why some may not want to use Python.
1. Most Python codes may run slower than Java or C++ code. However, many believe that a *programmer's time* is more valuable than the *CPU's time* and that is why they prefer to use python.
2. Python can be a difficult language to use when we are building highly concurrent and multi-threaded applications and mainly the applications with **CPU bound threads**.

## Important Libraries used in Python 
### 1. **Numpy** - *Numerical Python*
- provides data structures, algorithms and library glue that is necessary for the scientific applications that involve *numerical data* in Python.
- contains a fast and efficient multidimensional array objects called *ndarray*.
- contains functions to perform element - wise computations with arrays and mathematical operations between arrays.
- Linear algebra operations like *fourier transform* and *random number generations*.
- Numpy also serves as a *container for data* to be passed along algorithms and libraries.
### 2. **Pandas** - derived from *Panel Data*
- came into emergence in 2010.
- provides high level data structures and functions and that helps us work woth structured and tabular data in a *fast, easy and expressive way*.
- **Primary objects** in Pandas:
    - *DataFrames* - tabular and column oriented data structure that has both the rows and columns.
    - *Series* - one dimensional labeled array objects
- provides indexing functionality that helps us reshape, slice and dice, perform aggregations, and select subsets of data.
- this library is one of the primary focuses int he book as **data manipulation, data preparation and data cleaning** are important parts of data science.
### 3. **Matplotlib** 
- originally created by John D. Hunter and is now maintained by a large team of developers.
- most popular python library to produce plots and other two-dimensional data visualizations.
### 4. Ipython and Jupyter notebook 
- **Ipython**
    - The project had started in 2001 to develop a *more interactive* Python interpreter. 
    - designed to enhance your skills and productivity from the ground level in *interactive computing and software development*.
    - It encourages a workflow where you can execute and explore as you go unlike a workflow where you have to edit, complie and then run. 
- **Jupyter Notebook**
    - Developed in 2014 by the *Ipython team* and the *ipython web notebook* had turned into the *Jupyter web notebook* and was supported by 40 programming languages. 
    - IPython system can now be used as a *kernel or a programming language mode* for using Python with Jupyter.
### 5. **SciPy**
- a collection of packages that address a number of different standard problem domains in scientific computing.
- Some examples of the packages included are: 
    - `scipy.integrate` - Numerical Integration routines and diferential equation solvers.
    - `scipy.linalg` - Linear algebra routines and matrix decompositions extending beyond those provided
in `numpy.linalg`.
    - `scipy.stats` - A continuous and discrete probability distributions like density functions,
samplers, continuous distribution functions. It is also used for multiple statistical tests and descriptive statistics.
### 6. **scikit-learn**
- Came into existence in 2010.
- It has been the main *machine learning toolkit* for python programmers.
- Includes *submodules* for models like:
    - Regression: Lasso, ridge regression, etc.
    - Clustering: k-means, spectral clustering, etc.
    - Preprocessing: Feature extraction, normalization.
    - and many more...
### 7. **statsmodels**
- statistical analysis package created by the stats professor in Stanford University - Johnathan Taylor.
    - implemented many *regression analysis models* commonly popular in R programming language. 
- Similar to scikit-learn, statsmodels also contain algorithms for *classical(frequentist) statistics and econometrics*.
- It includes submodules like: 
    - Regression models: Linear Regression, Generalized regression models, etc.
    - Anaysis of Variance or ANOVA
    - Time series analysis: AR, ARMA, ARIMA and many other models.
 
## Other examples of Integrated Development Environments (IDE) and Text Editors
- There are benefits of using iPython with a text editor if you are writing a program and testing each partor section one after the other, but if you are doing software development, the following IDE's are recommended.
    - PyDev - an IDE built on Eclipse Platform.
    - PyCharm - built from JetBrains
    - Python tools for visual studio (for Windows users)
    - Spyder - IDE shipped with Anaconda
    - Komodo IDE
  
# Chapter 2 Notes
  
## The Python Interpreter
- Python is an interpreted language. 
- It runs by executing one program at a time. 
    - `python` command can be used in the python terminal to see the version of python installed and it is `!python` in Jupyter notebook. 
    - `exit()` interpreter is used to exit from the interpreter.
    
## iPython Basics
- `ipython` command is the command necessary to launch ipython from the command line. 
- python statements can be ran by typing them and pressing enter and you can just type the variables name and hit enter to see the result of the variable.
- You can also use Jupyter notebook while writing larger blocks of code over the iPython terminal.

## Jupyter Notebook
- interacts with *kernels* or implementations of the Jupyter interactive computing protocol in a number of programming languages.
- On many platforms it opens up automatically on your default web browser. 
- Many use Jupyter as a local computing environment. However, it can also be deployed on servers and accessed remotely.

## Tab Completion
- It is one of the major improvements over the standard Python shell.
- While entering expressions in shells, pressing the *Tab* key will search the namespace for any variables (objects, functions, etc.) trying to match the characters taht have been typed so far.

## Introspection
- Using a question mark before or after a variable gives information about it and this is called *Object Introspection*.
    ```
    c = [1, 2, 3]
    c?

    Output: 
        Type:        list
        String form: [1, 2, 3]
        Length:      3
        Docstring:  
        Built-in mutable sequence.
        If no argument is given, the constructor creates a new empty list.
        The argument must be an iterable if specified.
    ```
 - **"?"** can also be used in the scenario where a number of characters combined with the *wildcard(*)* will show us all of the names that are matching the wildcard expression. An *example* is shown below:
    ```
    np.*load*?
    
    Output: 
    np.__loader__
    np.load
    np.loads
    np.loadtxt  
    ```
## The %run Command
- One can run any file in a Python program inside the environment of their iPython session using **%run** command.
- The script used in the command is run in an empty namespace where no imports or variables are shown or defined. Accordingly, the behavior of it should be the same as running the program on the command line.
- If you want to give a script access to variables defined in the interactive namespace, we can use **%run -i** instead of the normal %run command. 
- *%load ipython_script_test.py* will allow you to see the entire script in the Jupyter notebook 
   
## Magic Commands
- These are *iPython special commands* that are also built into *magic commands*. 
- designed to facilitate common tasks and enable an individual to easily control the behavior of an IPython system. 
- A magic function can be used without the percentage sign, but there should be no other variables that have the same name as that specific *magic command*.

## Matplotlib Integration
- Ipython also integrates well with *data visualization* and other *user interface libraries* like **matplotlib**. 
    - `%matplotlib` magic function configures its integrations with an IPython shell or Jupyter notebook.
    1. Matplotlib command in *IPython shell*: `%matplotlib`. Matplotlib sets up integration so multiple plot windows can be created without interfering the console session.
    2. Matplotlib command in *Jupyter notebook*: `%matplotlib inline`. This command is used more often in the Jupyter notebook. 

## Python Language Basics

### 1. Python language semantics.
- They use tabs or spaces *(mainly whitespaces)* instead of braces to structure code like in R, C++, etc.

    ```
    for x in array:
        if x < pivot:
            less.append(x)
        else:
            greater.append(x)
    ```
    - *colon* - shows the start of an indentation block after which all lines of code must be indented to the same amount till the end of the block.
    - Python statements do not always need to be terminated with semi-colons. but they can be used to seperate multiple statements on one single line. *See the following example:* 
    `a = 5; b = 6; c = 7`
    
### 2. Object
- *object model* is an important characteristic of the Python language.
- *python object* is when every number, string, data structure, function, class, module and all exists in the Python interpreter in its own class.
    - Each *object* has an associated type (string, int) and its own internal data. 
    
### 3. Comments 
- **(#)** describes that something is a single line comment and is ignored by the interpreter. When you want to delete certain blocks of code without deleting them then this is a way. An example of multiple lines commented is shown *below*:
```
results = []
for line in file_handle:
# keep the empty lines for now
# if len(line) == 0:
# continue
results.append(line.replace('foo', 'bar'))
```

### 4. Functions and object method calls
- Functions that are using parentheses and passing zero or more arguments like in the second line below. You can also assign a return value to a variable like in the first line below. 
    `result = f(x, y, z)`
    `g()`
- Almost every object in Python has attached functions that are known as **methods** and they have access to the objects internal contents. they call be called using the syntax mentioned below:
    `obj.some_method(x, y, z)`
### 5. Variables and argument passing
- When we assign a variable or a name in Python, we are creating a reference to the object on the right side of the equal sign. One example can be the list below: 
    `a = [1, 2, 3]`
    - Let us assume to a new variable 'b':
    `b = a`
- In other languages, the list `[1, 2, 3]` would be copied into b. However, in python, both *a* and *b* refer to the same object or the original list  `[1, 2, 3]`. They point to the list instead of copying it into the object.
- If you bind a new object to a variable inside a specific function, the change will not be reflected in parent scope. It is therefore possible to alter the internals mutable arguments.

- `'5' + 5` - We cannot add a string to an int data type. We will get a *TypeError*. 
- If you divide a floating point number with a whole number then we end up getting a floating point number. If we *divide 4.5 by 2* then we get the number `2.25`

### 6. Attributes and methods
- Objects in Python have both *attributes* and *methods* Both can be accessed by the syntax, `obj.attribute_name`.
    - *attributes* :- objects that are stored inside the object.
    - *methods* :- functions asociated with an object that can also have access to the object's internal data.

### 7. Duck Typing
- This is when we can check that the object has certain *methods and behaviors* to understand that it is a specific method.
- The term *duck typing* comes from the saying: "If it walks like a duck ans quacks like a duck then it is a duck"
    - The statement above tells us that a method like quack() could show us that the object is of Duck type or a duck object.

### 8. Binary operators and comparisons
- To check if two references refer to the same object we use the *is* keyword. Example:
 `a is b` may return `true or false`
- One o the common use of *is and is not* is when we check if a variable is *None* as only one instance of *None* exists.
```
a = None
a is None

Output: True
```

### 9. Mutable and immutable objects
- Examples of *mutable objects*: lists, dicts, NumPy arrays, and most user-defined data types like clases.
- Examples of *immutable objects*: strings and tuples.

## Scalar Types
- Along with the standard library, Python has a small set of built-in types to handle numerical data, strings, booleans and dates/time.
    - These *single value* data are referred to a **scalar** data types
### 1. Numeric Types
- The primary *numeric types* in Python are **int** and **float**. Int have whole numbers only while float can have both whole numbers and decimals. 
    - Examples of Int: 3, 4, 5. It can arbirtrarily store large numbers.
    - Examples of Float: 3.4, 5.6, 29. Each float item is double precision or 64-bit value.
    
### 2. Strings
- Python is also known for its powerful and flexible built-in string processing capabilities.
    - One way to write strings is *single quotes* : `'one way'`
    - Second way to write strings is *double quotes* : `"second way"`
- We also have multi-line strings with line breaks written in the following format.
    ```
    """
    This is a longer string that
    spans multiple lines
    """
    ```
- Python strings are immutable and cannot be modified. 
- 'str' function can be used to convert other objects to string.

- *(+)* sign can be used in strings to merge two strings together.
-The example below merger a and b strings into one.
```
a = 'this is the first half '
b = 'and this is the second half'
a + b
```

### 3. Bytes and Unicode
- Unicode has turned into a *first-class string type* to enable more consistent handling of *ASCII and non-ASCII text*.
- In earlier times, strings were all *bytes* without much *Unicode encoding*.

### 4. Boolean
- Two boolean values are either written as **true** or **false**. Conditional expressions either evaluate to True or False. Boolean values are generally combines with '*and*' or '*or*' keywords.
`True and False evaluates to False`
`True or False evaluates to True`

### 5. Type casting
- *str, bool, int and float* types are also functions can also be used to cast values to those types. 
`True and False evaluates to False`
`True or False evaluates to True`
-Examples:
`
s = '3.14159'
fval = float(s) -This is a type conversion from string ot float.
`
### I gave a few examples. There are also many more scalar type examples.

## Control Flow
### 1. if elif and else
    - *If* first checks the initial condition and if it evaluates to true. 
    - Following that *elif* checks if a second conditions is true or not and returns that.
    - When none of them work, they look at the *Else* statement and return the statement returned by default. 
    
### 2. for loop
    - Acts as an iterator and iterates over each variable in a list, tuple, etc. Syntax examples         is:
    `
    for value in collection:
        # do something with value
    `
    - break keyword 
        - It only terminates the inner loop and the outer loops will continue to run. 

### 3. while loop
    - executes a condition and block of code until a *False* condition is reached or the loop
    ends with a break.
    
### 4. pass
    -can be used in the blocks where no action is expected to be taken, so it can just go on.
    
### 5. range
    -it will iterate and show a range of characters.
    
### 6. Ternary Expression
    - allows you to combine if-else statements into one line. 
    
### I gave a few common examples of control flow. There are also many more examples.



    

