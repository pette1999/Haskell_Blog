[Back](README.md)
# Modules

If you have used Java, you should know how to bind all classes into a  `package` folder named . Similarly, Haskell can treat this similar `package` concept as a module.

Haskell is a functional programming language. Everything is expressed as an expression. Therefore, a module is a collection of functions of similar or related types.

You can import functions from one module to another. Before starting to define the function, all `import` statements should be placed first. In this chapter, we will learn about the different functions defined and used in Haskell modules.

1. [List module](#List-module)
2. [Char module](#Char-module)
3. [Map module](#Map-module)
4. [Set Module](#Set-Module)

## 1. **List module**

List provides some great functions to handle list type data. After importing the `Data.List` module, you can use various functions. In the following example, `List` some important functions under the module are used.

```
main = do  
   putStrLn("Different methods of List Module") 
   print(intersperse '.' "Yiibai.com") 
   print(intercalate " " ["Lets","Start","with","Haskell"]) 
   print(splitAt 7 "HaskellTutorial") 
   print (sort [8,5,3,2,1,6,4,2])
```

Here, there are many functions that do not need to be defined. This is because these functions `List` are already defined and available in the module. After importing the `List` module, the Haskell compiler makes all these functions available in the global namespace.

Executing the above sample code will produce the following output:

```
Different methods of List Module
"Y.i.i.b.a.i...c.o.m"
"Lets Start with Haskell"
("Haskell","Tutorial")
[1,2,2,3,4,5,6,8]
```

## 2. **Char module**

`Char` The module has many predefined functions, which can be used with `Character` types. Take a look at the following code block:

```
main = do  
   putStrLn("Different methods of Char Module") 
   print(toUpper 'a') 
   print(words "Let us study tonight") 
   print(toLower 'A')
```

Here, the `toUpper` sum `toLower` function has been `Char` defined inside the module. Executing the above code will produce the following output:

```
Different methods of Char Module
'A'
["Let","us","study","tonight"]
'a'
```

## 3. **Map module**

Map is type data of unsorted key-value pairs. It is a widely used module with many useful functions. The following example shows how to use the predefined functions available in the Map module.

```
myMap :: Integer -> Map Integer [Integer] 
myMap n = Map.fromList (map makePair [1..n]) 
   where makePair x = (x, [x])  

main = print(myMap 3)
```

Execute the above sample code and get the following results:

```
fromList [(1,[1]),(2,[2]),(3,[3])]
```

## 4. **Set Module**

`Set` There are some very useful predefined functions in the module to process mathematical data. The collection is implemented as a binary tree, so all elements in the collection must be unique.

```
text1 = "Hey buddy"   
text2 = "This tutorial is for Haskell"   

main = do  
   let set1 = Set.fromList text1   
       set2 = Set.fromList text2 
   print(set1) 
   print(set2)
```

Here, we will `String` modify it to `Set`. It will produce the following output (the output set does not have repeated characters)

execute the above sample code, and get the following result:

```
fromList " Hbdeuy"
fromList " HTaefhiklorstu"
```
