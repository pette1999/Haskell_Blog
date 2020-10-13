[Back](README.md)
# Haskell Basic Data Model

Haskell is a purely functional programming language, so it is more interactive and intelligent than other programming languages. In this article, we will learn the basic data models of Haskell, which are actually predefined or intelligently decoded into computer memory in some way. 

1. [Numbers](#1-Numbers)
2. [Characters](#2-Characters)
3. [String](#3-String)
4. [Boolean](#4-Boolean)
5. [List](#5-List)
6. [Tuples](#6-Tuples)


## 1. **Numbers**

Haskell is smart enough to decode certain numbers into numbers. Therefore, there is no need to specify its data type externally as it is usually done in other programming languages. In the following example, enter the command prompt, then run it `2 + 2`and press **Enter** to get the result.

```shell
Peters-MBP:~ peter$ ghci
GHCi, version 8.8.4: https://www.haskell.org/ghc/  :? for help
Prelude> 2+2
```

You will receive the following output:

```
4
```

In the above code, only two numbers are passed as parameters to the GHCI compiler, but their types are not predefined, but the compiler can decode these two data items into numbers.
Next, try more complex mathematical calculations to see if the compiler can provide the correct output. Try to enter the calculation expression: `15+(5 * 5)- 40` as shown below:

```
Prelude> 15+(5*5)-40
```

The above expression as expected output is: `0`.

## 2. **Characters**

Like numbers, Haskell can recognize input characters. Go to the Haskell command prompt and enter any character with double quotes or single quotes. Look at the following input and output results.

```
Prelude> :t "a"
```

It will produce the following results:

```
"a" :: [Char]
```

Remember to use ( `:t`) when providing input . In the example above, `:t` specific types related to input will be included. Learn more about this type in the following chapters.
In the following example, we pass some invalid input as `char` it will cause an error.

```
Prelude> :t a

<interactive>:1:1: error: Variable not in scope: a
Prelude> a

<interactive>:8:1: error: Variable not in scope: a
Prelude> 
```

Through the error message `<interactive>:1:1: Not in scope: 'a'`, the Haskell compiler warns that it cannot recognize the input. Haskell is a language and all content is represented by numbers. Haskell follows the conventional ASCII encoding style. You can take a look at the example below to learn more −

```
Prelude> '\97'
'a'
```

## 3. **String**

A string is a collection of characters. There is no specific syntax for using strings, but Haskell follows the regular style of using double quotes to represent strings. Look at the example below, passing a string "peterchen".

```
Prelude> :t "peterchen"
"peterchen" :: [Char]
```

## 4. **Boolean**

The Boolean data type is also very similar to other data types. In the following example, we will use some Boolean inputs (for example, `True` or `False`) to use different Boolean operations.

```
Prelude> True && True
True
Prelude> True && False
False
Prelude> True || True
True
```

In the example above, it is not necessary to explain that the `True` sum `False` is a Boolean value. Haskell itself can decode it and perform corresponding operations. The following modification is used `true` or `false` as input.

```
Prelude> true

<interactive>:16:1: error:
    • Variable not in scope: true
    • Perhaps you meant data constructor ‘True’ (imported from Prelude)
```

In the example above, Haskell cannot distinguish between `true` numeric values ​​because the input `true` is not a number. Therefore, the Haskell compiler will raise an error stating that the input is not in its scope.

## 5. **List**

Like other data types, List is a very useful data type used in Haskell. According to the example, it `[a，b，c]` is a list of characters, so by definition, List is a collection of the same data type separated by commas.
As with other data types, there is no need to declare the data as a List. Haskell can decode the input by looking at the syntax used in the expression.
The following example demonstrates how Haskell handles lists.

```
Prelude> [1,2,3,4,5,6,7]
[1,2,3,4,5,6,7]
```

Lists in Haskell are essentially the same type, so they are not allowed to declare lists of different data types. [1,2,3,a,b,c]A list like this will produce errors.

```
Prelude> [1,2,3,a,b,c]

<interactive>:18:8: error: Variable not in scope: a

<interactive>:18:10: error: Variable not in scope: b

<interactive>:18:12: error: Variable not in scope: c
```

### **List Comprehension**

List comprehension is the process of generating lists using mathematical expressions. Please take a look at the example below, where mathematical expressions are used in the form of [output| range, condition].

```
Prelude> [x*2| x<-[1..10]]
[2,4,6,8,10,12,14,16,18,20]
```

This method of creating lists using mathematical expressions is called **list comprehension**.

## 6. **Tuples**

Haskell provides another way to declare multiple values ​​in a single data type. It is called a tuple. Tuples can be regarded as lists, but there are some technical differences between tuples and lists.
Tuple is an immutable data type, because the number of elements cannot be modified at runtime, and the list is a mutable data type, and the list is a homogeneous data type, but Tuple is heterogeneous in nature, because Tuple may contain Different types of data. Tuples are represented by a single bracket. Take a look at the following example to understand how Haskell handles tuples.

```
Prelude> (1,1,'a')
(1,1,'a')
```

In the above example, `char` a tuple with two numeric type variables and one type variable is used.