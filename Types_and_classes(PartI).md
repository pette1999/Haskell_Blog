[Back](README.md)
# Haskell types and Type classes (Part I)

Haskell is a functional language. It is strictly typed. The Haskell compiler knows the data types used in the entire application at compile time.

1. [Built-in type classes](#1.-**Built-in-type-classes**)
2. [Int](#2.-**Int**)
3. [Integer](#3.-**Integer**)
4. [Float](#4.-**Float**)
5. [Double](#5.-**Double**)
6. [Bool](#5.-**Bool**)
7. [Char](#5.-**Char**)

## 1. **Built-in type classes**

In Haskell, each statement is treated as a mathematical expression, and the category of this expression is called type ( `Type` ). It can be said that it `Type` is the data type of the expression used at compile time.

To learn more about types, you can use `:t` commands. In a general way, you can think of a type as a value, and a type class as a group of similar types. In this chapter, we will learn about the different built-in types.

## 2. **Int**

`Int` Is `Integer` a type class representing type data. Every integer `2147483647` in the `-2147483647` range belongs to the `Int` type class. In the following example, the function `fType()` will be represented according to the defined type.

```
fType :: Int -> Int -> Int 
fType x y = x*x + y*y
main = print (fType 2 4)
```

Here, we set `fType()` the type of the function to `int`. The function takes two `int` values ​​and returns one `int` value. If this code is compiled and executed, it will produce the following output:

```
20
```

## 3. **Integer**

`Integer` Can be regarded as `Int` a superset. This value is not restricted by any number, so it `Integer` can be any length without any restriction. To understand the basic difference between type `Int` and `Integer` type, modify the above code as follows:

```
fType :: Int -> Int -> Int 
fType x y = x*x + y*y 
main = print (fType 212124454 44545454454554545445454544545)
```

If you compile the above code, the following error message will be thrown:

```
main.hs:3:31: Warning:            
   Literal 44545454454554545445454544545 is out of the Int range -
   9223372036854775808..9223372036854775807 
Linking main ...
```

This error occurs because the function `fType()` expects a `Int` type value and some large `Int` type values are passed . To avoid this error, the `Int` type will be modified `Integer` and the difference will be observed.

```
fType :: Integer -> Integer -> Integer 
fType x y = x*x + y*y 
main = print (fType 212124454 4454545445455454545445445454544545)
```

Now, it will produce the following output:


```
1984297512562793395882644631364297686099210302577374055141
```

## 4. **Float**

```
fType :: Float -> Float -> Float 
fType x y = x*x + y*y 
main = print (fType 2.5 3.8)
```

This function takes two floating-point values ​​as input and produces another floating-point value as output. When this code is compiled and executed, it will produce the following output:

```
20.689999
```

## 5. **Double**

`Double` It is a floating-point number with double precision at the end. Look at the sample code below:

```
fType :: Double -> Double -> Double 
fType x y = x*x + y*y 
main = print (fType 2.56 3.81)
```

When this code is compiled and executed, it will produce the following output:

```
21.0697
```

## 6. **Bool**

Bool is a Boolean type. Its value can be `True` OR `False`. Execute the following code to understand how `Bool` types work in Haskell.

```
main = do  
   let x = True 

   if x == False 
      then putStrLn "X matches with Bool Type" 
   else putStrLn "X is not a Bool Type"
```

Here, we define the variable `x` as a boolean and compare it with another boolean to check its value. When this code is compiled and executed, it will produce the following output:

```
X is not a Bool Type
```

## 7. **Char**

`Char` Represents characters. Everything within single quotes is treated as characters. In the code below, we modified the previous `fType()` function to accept a `Char` value and `Char` return the value as output.

```
fType :: Char-> Char 
fType x = 'K' 
main = do  
   let x = 'v' 
   print (fType x)
```

The above code will call the `fType()` function with the parameter as the `char` type value `v`, but it will return another `char` value, ie `K`. Here is its output:

```
'K'
```