[Back](README.md)
# Function Composition

Function composition is the process of using the output of one function as the input of another function. In mathematics, composition is `f{g(x)}` represented `g()` by a function whose output is used as `f()` the input of another function (ie ).

If the output type of one function matches the input type of the second function, you can use these two functions to achieve function combination. We use the dot operator ( `.`) to implement function composition in Haskell.

Look at the sample code below. Demonstrate how to use function combination to calculate whether the input number is even or odd.

```
eveno :: Int -> Bool 
noto  :: Bool -> String 

eveno x = if x `rem` 2 == 0 
   then True 
else False 
noto x = if x == True 
   then "This is an even Number" 
else "This is an ODD number" 

main = do 
   putStrLn "Example of Haskell Function composition" 
   print ((noto.eveno)(16))
```

Here, in the `main` function, two functions `noto` and are called at the same time `eveno`. The compiler will first call it with the function `16` as a parameter `eveno()`. Thereafter, the compiler will use `eveno` the output of the `noto()` function as the input of the function.

The output of executing the above sample code is as follows −

```
Example of Haskell Function composition                
"This is an even Number"
```

By providing a digital `16` as input (which is even), and therefore `eveno()` function returns the `true` resulting `noto()` function of the input and output returns: `"This is an even Number"`.