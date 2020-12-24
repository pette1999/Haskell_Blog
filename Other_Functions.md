[Back](README.md)
# Other Functions

So far, we have discussed many types of Haskell functions and used different ways to call these functions. In this chapter, you will learn some basic functions that can be easily used in Haskell without importing any special `Type` classes. Most of these functions are part of other high-level functions.

1. [head function](#head-function)
2. [tail function](#tail-function)
3. [The last function](#The-last-function)
4. [init function](#init-function)
5. [Null function](#Null-function)
6. [The reverse function](#The-reverse-function)
7. [length function](#length-function)
8. [take function](#take-function)
9. [drop function](#drop-function)
10. [Maximum function](#Maximum-function)
11. [minmum function](#minmum-function)
12. [Sum function](#Sum-function)
13. [product function](#product-function)
14. [elem function](#elem-function)

## 1. **head function**

The Head function is suitable for lists. It returns the first input parameter, which is basically a list. In the following example, we pass a `10` list of values ​​and use the `head` function to return the first element of the list.

```
main = do 
   let x = [1..10]   
   putStrLn "Our list is:"  
   print (x) 
   putStrLn "The first element of the list is:" 
   print (head x)
```

Execute the above sample code and get the following results:

```
Our list is: 
[1,2,3,4,5,6,7,8,9,10]
The first element of the list is:
1
```

## 2. **tail function**

`tail` Function is `head` a complement to function. It takes a list as an input parameter and produces the entire list without a header. `tail` The function will return the entire list without the first element. Look at the following example-

```
main = do 
   let x = [1..10]   
   putStrLn "Our list is:"  
   print (x) 
   putStrLn "The tail of our list is:" 
   print (tail x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5,6,7,8,9,10]
The tail of our list is:
[2,3,4,5,6,7,8,9,10]
```

## 3. **The last function**

As the name suggests, the last function gets the last element of the list. Check out the following example:

```
main = do 
   let x = [1..10]   
   putStrLn "Our list is:"  
   print (x) 
   putStrLn "The last element of our list is:" 
   print (last x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5,6,7,8,9,10]
The last element of our list is:
10
```

## 4. **init function**

`init` Functions `tail` are completely opposite to functions. It takes a list as a parameter and returns the entire list, but does not include the last entry.

```
main = do 
   let x = [1..10]   
   putStrLn "Our list is:"  
   print (x) 
   putStrLn "Our list without the last entry:"  
   print (init x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5,6,7,8,9,10]
Our list without the last entry:
[1,2,3,4,5,6,7,8,9]
```

## 5. **Null function**

The Null function is a Boolean check function. It works on strings and returns only when the given list is empty `True`, otherwise it returns `False`. The following code checks whether the provided list is empty.

```
main = do 
   let x = [1..10]   
   putStrLn "Our list is:"  
   print (x) 
   putStrLn "Is our list empty?"  
   print (null x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5,6,7,8,9,10]
Is our list empty?
False
```

## 6. **The reverse function**

It works on string input and converts the entire input to the reverse order, and reverses the output. The following is the sample code of this function:

```
main = do 
   let x = [1..10]  
   putStrLn "Our list is:" 
   print (x) 
   putStrLn "The list in Reverse Order is:" 
   print (reverse x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5,6,7,8,9,10]
The list in Reverse Order is:
[10,9,8,7,6,5,4,3,2,1]
```

## 7. **length function**

This function is used to calculate the length of the parameter. Look at the following example-

```
main = do 
   let x = [1..10]   
   putStrLn "Our list is:" 
   print (x) 
   putStrLn "The length of this list is:" 
   print (length x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5,6,7,8,9,10]
The length of this list is:
10
```

## 8. **take function**

`take` Functions are used to create substrings from a string. The following code shows how to use `take` functions in Haskell −

```
main = print(take 5 ([1 .. 10]))
```

Execute the above sample code and get the following results:

```
[1,2,3,4,5]
```

## 9. **drop function**

`drop` Functions are also used to generate substrings. Its `take` function is opposite to function. Look at the code below-

```
main = print(drop 5 ([1 .. 10]))
```

The above code deletes the first 5 elements in the list and prints the remaining 5 elements. It will produce the following output-

```
[6,7,8,9,10]
```

## 10. **Maximum function**

`maximum` The function is used to find the element with the largest value from the provided list. See how to use it in code-

```
main = do 
   let x = [1,45,565,1245,02,2]   
   putStrLn "The maximum value element of the list is:"  
   print (maximum x)
```

Execute the above sample code and get the following results:

```
The maximum value element of the list is:
1245
```

## 11. **minmum function**

`minmum` The function is used to find the smallest element from the provided list. See how to use it in code-

```
main = do 
   let x = [1,45,565,1245,02,2]   
   putStrLn "The minimum value element of the list is:"  
   print (minimum x)
```

Execute the above sample code and get the following results:

```
The minimum value element of the list is:
1
```

## 12. **Sum function**

As the name suggests, this function returns the sum of all elements present in the provided list. The following code gets a list of 5 elements and returns the sum as output.

```
main = do 
   let x = [1..5] 
   putStrLn "Our list is:" 
   print (x) 
   putStrLn "The summation of the list elements is:" 
   print (sum x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5]
The summation of the list elements is:
15
```

## 13. **product function**

You can use this function to multiply all the elements in the list and print their values. Refer to the following sample code:

```
main = do 
   let x = [1..5] 
   putStrLn "Our list is:" 
   print (x) 
   putStrLn "The multiplication of the list elements is:" 
   print (product x)
```

Execute the above sample code and get the following results:

```
Our list is:
[1,2,3,4,5]
The multiplication of the list elements is: 
120
```

## 14. **elem function**

`elem` The function is used to check whether the list contains a specific element. Return if it contains `true`, otherwise return `false`. The following code checks whether the provided element list contains a value `786`.

```
main = do 
   let x = [1,45,155,1785] 
   putStrLn "Our list is:" 
   print (x) 
   putStrLn "Does it contain 786?" 
   print (elem 786 (x))
```

Execute the above sample code and get the following results:

```
Our list is:
[1,45,155,1785]
Does it contain 786?
False
```

