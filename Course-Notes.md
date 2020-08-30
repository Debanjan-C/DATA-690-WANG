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

# Introspection
- Using a question mark before or after a variable gives information about it and this is called *Object Introspection*.

    -c = [1, 2, 3]
    -c?

    -Output: 
        -Type:        list
        -String form: [1, 2, 3]
        -Length:      3
        -Docstring:  
        -Built-in mutable sequence.
        -If no argument is given, the constructor creates a new empty list.
        -The argument must be an iterable if specified.
`c`
