# Introduction to Haskell

Haskell is a functional programming language specifically designed to handle symbolic calculations and list processing applications. Functional programming is based on mathematical functions. In addition to Haskell, other popular languages ​​that follow the functional programming paradigm include: Lisp, Python, Erlang, Racket, F#, Clojure, etc.

In conventional programming, instructions are regarded as a set of declarations in a specific syntax or format, but in functional programming, all calculations are regarded as a combination of independent mathematical functions.

## Programming with Haskell functions

Haskell is a widely used purely functional language. Here, we have listed a few points that make the Haskell language so different from other conventional programming languages ​​(such as Java , C, C++, PHP, etc.).

- Functional Language - In traditional programming languages, the compiler is instructed to perform a series of tasks that only tell the computer "what to do" and "how to do". But in Haskell only tells the computer "what is this?".

- Laziness - Haskell is a lazy language. Laziness means that Haskell will not immediately evaluate the calculation expression. When the evaluation calculation engine finds that an expression needs to be evaluated, it creates a thunk data structure to collect all the information needed for that particular evaluation and a pointer to the thunk data structure. The evaluation calculation engine only starts working when a specific expression needs to be evaluated.

- Modularity - Haskell application is a series of functions. A Haskell application is a collection of many small Haskell applications.

- Static Typing - In conventional programming languages, a series of variables and their types need to be defined. And Haskell is a strictly typed language. Expressed in a strictly typed language, the Haskell compiler is smart enough to figure out the type of the declared variable, so there is no need to explicitly mention the type of the variable used.

- Maintainability - Haskell applications are modular, so maintaining them is very easy and cost-effective.

Functional programs have higher concurrency. They follow parallelism during execution to provide more accurate and better performance. Haskell is no exception. It is developed in a way that effectively handles multithreading.

## HELLO WORLD program

This is a simple example to demonstrate the dynamics of Haskell. The following code only needs one line to be printed on the console "Hello Word". 
`main = putStrLn "Hello World"`
 The Haskell compiler interprets and executes the above code, it will immediately produce the following output
` Hello World`
