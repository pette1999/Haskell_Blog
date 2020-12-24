[Back](README.md)
# Haskell types and Type classes (Part II)

Haskell is a functional language. It is strictly typed. The Haskell compiler knows the data types used in the entire application at compile time.

8. [EQ Type Class](#8-EQ-Type-Class)
9. [Ord type class](#9-Ord-Type-Class)
10. [Show](#10-Show)
11. [Read](#11-Read)
12. [Enum](#12-Enum)
13. [Bounded](#13-Bounded)
14. [Num](#14-Num)
15. [Integral](#15-Integral)
16. [Floating](#16-Floating)
17. [Custom Type Class](#17-Custom-Type-Class)

## 8. **EQ Type Class**

The EQ type class is an interface that provides a function to test whether expressions are equal. The type classes that check whether the expressions are equal should belong to this EQ type class.

All the standard type classes mentioned above are part of this EQ class. Whenever we use any of the above types to check any equality, we are actually calling the EQ type class.

In the following example, the EQ type is used internally `==` or `/=` operated.

```
main = do 
   if 8 /= 8 
      then putStrLn "The values are Equal" 
   else putStrLn "The values are not Equal"
```

It will produce the following output:

```
The values are not Equal
```

## 9. **Ord Type Class**

Ord is another interface class that provides sorting functions. All types used so far are `Ord` part of the interface. Similar to the EQ interface, you can use the `>`, `<`, `<=`, `>=`, `compare` to call Ord interface.

Use the "compare" function of this type class in the following example.

```
main = print (4 <= 2)
```

Here, the Haskell compiler will check `4` if it is less than or equal to `2`. Since it `4` is not less than or equal to `2`, the code will produce the following output:

```
False
```

## 10. **Show**

`Show` It has the function of printing parameters as character strings. No matter what the parameter is, it always prints the result as a string. In the following example, we will use this interface to print the entire list.

`Show` Can be used to call this interface.

```
main = print (show [1..10])
```

It will produce the following output on the console. Here, the double quotation marks indicate that it is a string type value.

```
"[1,2,3,4,5,6,7,8,9,10]"
```

## 11. **Read**

`Read` The function of the interface is the same as the display, but the result is not printed in string format. In the following code, use the `read` interface to read a string value and convert it to a `Int` value.

```
main = print (readInt "12") 
readInt :: String -> Int 
readInt = read
```

Here, the string variable ( `"12"`) is passed to the `readInt` method, which returns `12`(Int value) after conversion . Here is its output:

```
12
```

## 12. **Enum**

Enumerations are `Type` another type of class that can enable sequential or ordered functions in Haskell. Through techniques such as `Succ`, `Pred`, `Bool`, `Char` to access this other command `Type` type.

The following code shows how to find `12` the successor value:

```
main = print (succ 12)
```

It will produce the following output on the console:

```
13
```

## 13. **Bounded**

Having upper and lower limits of all types belong to this `Type` category. For example, `Int` the maximum range of type data is `9223372036854775807`, and the minimum range is `-9223372036854775808`.

The following code shows how Haskell determines `Int` the maximum and minimum range of a type.

```
main = do 
   print (maxBound :: Int) 
   print (minBound :: Int)
```

It will produce the following output on the console:

```
9223372036854775807
-9223372036854775808
```

## 14. **Num**

`Num` Type classes are used for number operations. Such as `Int`, `Integer`, `Float` and the `Double` type and the like fall into this `Type` category. Take a look at the code below-

```
main = do 
   print(2 :: Int)  
   print(2 :: Float)
```

It will produce the following output on the console:

```
2
2.0
```

## 15. **Integral**

Integers can be considered as `Num Type` subclasses of the class. `Num Type` The class holds all types of numbers, while the `Integral` type class is only used for integers. `Int` And `Integer` it is of this `Type` type under the category.

## 16. **Floating**

Like the `Integral` same, it `Floating` is also `Num Type` part of the class, but it only contains floating point numbers. Therefore, `Float` and `Double` belong to this type.

## 17. **Custom Type Class**

Like any other programming language, Haskell allows developers to define user-defined types. In the following example, we will create a user-defined type and use it.

```
data Area = Circle Float Float Float  
surface :: Area -> Float   
surface (Circle _ _ r) = pi * r ^ 2   
main = print (surface $ Circle 10 20 10 )
```

Here, a `Area` new type named is created . Next use this type to calculate the area of ​​the circle. In the example above, it `surface` is a function that will take `Area` as input and produce `Float` as output.

It will produce the following output:

```
314.15927
```