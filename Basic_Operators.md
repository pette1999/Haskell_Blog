[Back](README.md)
# Haskel basic operators

Like other programming languages, Haskell can intelligently handle some basic operations, such as addition, subtraction, and multiplication. In the following chapters, we will learn more about the different operators and their usage.

1. [Addition](#1-Addition)
2. [Subtraction](#2-Subtraction)
3. [Multiplication](#3-Multiplication)
4. [Division](#4-Division)
5. [Sequence/range](#5-Sequence/range)

## 1. **Addition**

As the name suggests, the addition ( `+` ) operator is used for addition functions. The following sample code shows how to add two integers in Haskell:

```
main = do 
   let var1 = 2 
   let var2 = 3 
   putStrLn "The addition of the two numbers is:" 
   print(var1 + var2)
```

In the above file, we created two separate variables `var1` and `var2` finally printed the result using the addition operator.
This code will produce the following output on the screen:

```
The addition of the two numbers is:
5
```

## 2. **Subtraction**

As the name implies, the subtraction operator is used for subtraction operations. The following sample code shows how to subtract two integers in Haskell:

```
main = do 
   let var1 = 10 
   let var2 = 6 
   putStrLn "The Subtraction of the two numbers is:" 
   print(var1 - var2)
```

In this example, we created two variables `var1` and `var2`. After that, use the subtraction ( `-` ) operator to subtract the two values.
This code will produce the following output on the screen after execution:

```
The Subtraction of the two numbers is:
4
```

## 3. **Multiplication**

The multiplication operator is used for multiplication operations. The following code shows how to use the multiplication operator to multiply two numbers in Haskell:

```
main = do 
   let var1 = 2 
   let var2 = 3 
   putStrLn "The Multiplication of the Two Numbers is:" 
   print(var1 * var2)
```

This code will produce the following output on the screen after execution:

```
The Multiplication of the Two Numbers is:
6
```

## 4. **Division**

Take a look at the following code, which demonstrates how to divide two numbers in Haskell:

```
main = do 
   let var1 = 12 
   let var2 = 3 
   putStrLn "The Division of the Two Numbers is:" 
   print(var1/var2)
```

This code will produce the following output on the screen after execution:

```
The Division of the Two Numbers is: 
4.0
```

## 5. **Sequence/range**

Sequence or Range is a special operator in Haskell, which is used `..` to express. You can use this operator when declaring a list with a series of values.

If you want to print all values ​​from 1 to 10, you can use a similar`[1..10]` form. Similarly, if you want to generate all letters from ato z, you just need to type `[[a..z]`.

The following code shows how to use sequence operators to print all values ​​from 1 to 10:

```
main :: IO() 
main = do 
   print [1..10]
```

This code will produce the following output on the screen after execution:

```
[1,2,3,4,5,6,7,8,9,10]
```