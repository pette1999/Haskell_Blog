[Back](README.md)
# Input And Output

All the examples we have discussed so far are static in nature. In this chapter, we will learn how Haskell interacts with users dynamically. Learn the different input and output techniques used in Haskell.

1. [Files and streams](#1-Files-and-streams)
2. [Command line parameters](#2-Command-line-parameters)
3. [Abnormal](#3-Abnormal)

## 1. **Files and streams**

So far, we have hard-coded all the inputs in the program itself. In the previous study, we have obtained input from static variables. In this section, we learn how to read and write from external files.

Create a file and name it temp.txt . Next, enter the following line in this text file: `"Welcome to Peter's Haskell Blog."`

Next, we will write the following code, which will display the contents of the abc.txt file on the console . Use functions `readFile()` to read the file until a `EOF` character is found .

```
main = do  
   let file = "temp.txt" 
   contents <- readFile file 
   putStrLn contents
```

The above code will read the contents of the file `temp.txt` as a string until it encounters any end-of-file characters. This code will generate the following output:

```
Welcome to Peter's Haskell Blog.
```

## 2. **Command line parameters**

Haskell also provides the ability to manipulate files through the command prompt. Go to the terminal and type `ghci`. Then, type the following command set-

```
let file = "temp.txt" 
writeFile file "I am just experimenting here." 
readFile file
```

Here, we created a text file called abc.txt . Next, use the command `writeFile` to insert a line of content into the file. Finally, use the `readFile` command to print the contents of the file on the console. After executing the code, the following output is produced:

```
I am just experimenting here.
```

## 3. **Abnormal**

You can think of exceptions as errors in the code. In this case, the compiler cannot get the expected output at runtime. Like other good programming languages, Haskell provides a way to implement exception handling.

If you are familiar with Java, you probably know the `Try-Catch` block, and you usually raise an exception error in the `catch` block and catch the exception error in the block. In Haskell, we also have the same function of catching runtime errors.

`try` The function definition is similar `try :: Exception e => IO a -> IO (Either e a)`. Look at the sample code below, it shows how to catch the "divide by zero" exception.

```
main = do 
   result <- try (evaluate (5 `div` 0)) :: IO (Either SomeException Int) 
   case result of 
      Left ex   -> putStrLn $ "Caught exception: " ++ show ex 
      Right val -> putStrLn $ "The answer was: " ++ show val
```

In the above example, `Control.Exception` the built-in `try` function of the module is used , so the exception is caught in advance. The above code snippet will produce the following output on the screen:

```
Caught exception: divide by zero
```