## Chapter 1 Notes

# Kinds of Data
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
 
# Python
1. First appearance was in 1991 and it was one of the most popular interpreted programming languages with Ruby, Perl and any others.
    - Since 2005, Python and Ruby have become a great option for developing websites using a number of 
      frameworks like Django for Python and Rails for Ruby.
    - These languages are called scripting languages as they can be used to write small programs or      scripts and use it to automate other tasks. 
2. Python is one of the most important languages for Data Science, Machine Learning and general Software Engineering in academia and many industries.
    - In terms of data analysis, interactive computing and data visualization, python has similarities with other programming languages like R, MATLAB, SAS, STATA and many others. 

# Why some may not want to use Python.
1. Most Python codes may run slower than Java or C++ code. However, many believe that a *programmer's time* is more valuable than the *CPU's time* and that is why they prefer to use python.
2. Python can be a difficult language to use when we are building highly concurrent and multi-threaded applications and mainly the applications with **CPU bound threads**.

 # Important Libraries used in Python 
 1. **Numpy** - *Numerical Python*
     - provides data structures, algorithms and library glue that is necessary for the scientific applications that involve *numerical data* in Python.
     - contains a fast and efficient multidimensional array objects called *ndarray*.
     - contains functions to perform element - wise computations with arrays and mathematical operations between arrays.
     - Linear algebra operations like *fourier transform* and *random number generations*.
     - Numpy also serves as a *container for data* to be passed along algorithms and libraries.
2. **Pandas** - derived from *Panel Data*
    - came into emergence in 2010.
    - provides high level data structures and functions and that helps us work woth structured and tabular data in a *fast, easy and expressive way*.
    - **Primary objects** in Pandas:
        - *DataFrames* - tabular and column oriented data structure that has both the rows and columns.
        - *Series* - one dimensional labeled array objects
    - provides indexing functionality that helps us reshape, slice and dice, perform aggregations, and select subsets of data.
    - this library is one of the primary focuses int he book as **data manipulation, data preparation and data cleaning** are important parts of data science.
3. **Matplotlib** 
    - originally created by John D. Hunter and is now maintained by a large team of developers.
    - most popular python library to produce plots and other two-dimensional data visualizations.
