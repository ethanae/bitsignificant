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
char initial;
```  
Above is a variable called 'initial' which is of type _char_ that can only hold a single character at a time. This may hold the first character of a person's first name.  
  
```
string name;
```  
Here we are calling a variable 'name', that might hold a person's name, which can only hold `string`s which is an interesting type as we'll see later, but for now, it is a combination of characters to form words or sentences.  
  
```
bool isRetired;
```  
Here we have a variable called `isRetired` which might tell us whether if a person is retired or not. `bool`s are boolean types in that they can only hold `true` or `false`.
  
Take note of the names of our variables we have decided on. It is easy to reason about the types but just looking at their names. For instance, by looking at the 'age' variable above it is easy to see that by its name it should only hold integers. Similarly, the variable 'name' should hold someone's name and is a combination of characters which form something readable. 

A variable's name should describe the data it is intended to hold.

### Variable Initialisation
Variables without any data aren't very useful to us. Once our variables are declared we can start giving them data to store.

Initialisation means we are giving our newly declared variable a value for the first time. The way to do this is through variable assignment using the assignment operator. 

Taking the age example from the snippet above:  
```
age = 32;
```  
Our 'age' variable now stores the integer 32!  
Note that we don't have to specify the variable type again, we just type which variable to which we want to assign data.

Similarly, for our other variables that we've previously declared:  

```
name = "John Doe";

initial = 'J';

isRetired = false;
```

Some things to notice:
1. We use double quotes to create `string`s
2. We use single quotes to create `char`s
3. Valid boolean values are only `true` and `false`

### Declaration and Initialisation
More often that not we want to store some data inside our variables as soon as we declare them. The following is quite can become tedious to write in large programs.

```
int age;
age = 65;
```
  
Instead we can combine the above two lines into one, which saves us some typing:  
```
int age = 65;
```
  
### Tips and Tricks
In C#, there is some short-hand syntax when initialising a variable right away. Remember that every variable has a type so that both humans and compiler knows what data it can hold.

If you know what the type of data you want your variables to hold then you can do the following:  
```
var age = 11; // this is an integer!
var name = "John Doe"; // this is a string!
var isRetired = false; // this is a boolean!
var initial = 'J'; // this is a char!
```  
Notice we used the _var_ keyword here which replaces the variable _type_ we were using previously. The _var_ keyword is special because it tells the compiler that we are still declaring a variable as always but we telling the compiler to *infer* the type of our variable!

This is called type inference, but the compiler can only infer the variable type when we immediately give it a value. For instance, the snippet below results in an error:  
```
var age; // this is not allowed because the compiler has no idea what type to attribute to our variable!
```  
To fix this, when we use _var_ we must always give our variables values right away:  
```
var age = 11; // and the compiler correctly infers our age variable to be of type integer!
```
