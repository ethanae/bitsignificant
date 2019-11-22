# BitSignificant CSharp

## 2. Variables and Assignments

When we refer to variables in any given program we are talking about temporary identifiers with which we associate values. Every variable has a _type_ (we'll cover _types_ in later sections) but for now keep in mind that every variable has a _type_ and only allows values of that same type to be stored within it.

The power of variables come from their ability to hold our data, allow us to access and read it, run operations on it, and store it back into the same variable or other variables.

Note: variables are just human-readable identifiers of data and it is important to give your variables appropriate and meaningful names.

### Variable Declaration
#### Declaring a variable means that we give a name to an identifier that doesn't hold any data yet. This is an important distinction between variable declaration and variable initialistion. 

#### Variable declaration syntax is mostly the same across different language; first we decide the variable type (the kind of data it will hold, integers, doubles, strings, characters, booleans, etc.), then we decide on a name for our variable.

```
int age;
```  
Above is a declartion of an variable called age that will only old any single integer.  
  
```
string name;
```  
Here we are calling a variable 'name', that might hold a person's name, which can only hold `string`s which is an interesting type as we'll see later, but for now, it is a combination of characters to form words or sentences.  
  
```
bool isRetired;
```  
Here we have a variable called `isRetired` which might tell us whether if a person is retired or not. `bool`s are boolean types in that they can only hold `true` or `false`.
  
```
char initial;
```  
Above is a variable called 'initial' which is of type _char_ that can only hold a single character at a time. This may hold the first character of a person's first name.  
  
Take note of the names of our variables we have decided on. It is easy to reason about the types but just looking at their names. For instance, by looking at the 'age' variable above it is easy to see that by its name it should only hold integers. Similarly, the variable 'name' should hold someone's name and is a combination of characters which form something readable. 

A variable's name should describe the data it will eventually hold.

### Variable declaration
