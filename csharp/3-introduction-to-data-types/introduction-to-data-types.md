# BitSignificant CSharp

## 3. An Introduction to Data Types

### Data types form an integral part of any programming language. For now, we are going to explore some basic types provided to us by the language itself. These types are called _primitive data types_ because they are the usually the most basic types.

### We're going to look at the primitive types listed below:
- `boolean`
- `int`
- `double`
- `float`
- `boolean`
- `char`
- `string`

### 1. Boolean 
A boolean type refers to the values `true` and `false` only. This type gives us the ability to model true/false cases in our code. As you saw in our previous example we saw the declaration of a variable called `isRetired`, we could use this variable to determine if a user is a pensioner and then discount to some item they want to purchase.  

We can use the boolean value like this:
```
if (isRetired) 
{
    // some code to apply our discount
} 
else 
{

}
```

For illustration purposes, we've used a new construct called the _if-else-statement_ which helps us here which tests the value of a boolean type. These structures are part of _control flow_ which we'll cover in detail later on, so don't worry about it too much now.  

#### Boolean operations
As we saw above an, _if-else-statement_ can be used to test a boolean value but we can form much more complex expressions with boolean types.

Let's introduce another variable called `isStoreMember` which tells us if a customer is a member of our imaginary store, and we want to give customers discount if they're pensioners AND (`&&`) they're members at our store. Our program might look like:   
```
var isRetired = true;
var isStoreMember = true;
var shouldApplyDiscount = isRetired && isStoreMember;

if (shouldApplyDiscount) 
{
    // some code to apply our discount
}
```  
Here we are using a new-looking symbol, the double ampersand, `&&`. When we use this syntax we are creating an expression, in this case a boolean expression. You should read `&&` as "AND", which means that both values on either side of the double ampersand should be `true` for the whole expression to be true.

Note that we also get a single ampersand operator, `&`. Firstly, remember that `&&` needs to both values on either side to be true which means if the first operand is `false` we already know that the whole expression cannot possibly be true because we've already encountered a `false` value meaning that we do not need to even evaluate the rest of remaining expression (this is called short-circuiting). So, `&&` can short-circuit expression evaluation. 
  
We also get a single ampersand, `&`, operator that works a little differently compared to `&&`, in that it will always evaluate all operands of our expression but the end value remains the same as `&&`. So if either operand is `false`, our whole expression with be `false` otherwise all operands are `true` and our whole expression is `true`.

Some examples:  
```
var isRetired = false;
var isStoreMember = true;
var shouldApplyDiscount = isRetired && isStoreMember; // here isRetired is false which means our program doesn't need to evaluate isStoreMember and shouldApplyDiscount will be false
```

```
var isRetired = false;
var isStoreMember = true;
var shouldApplyDiscount = isRetired & isStoreMember; // isRetired is false again but all operands are evaluated but shouldApplyDiscount is still false
```

It helps to think of `&&` and `&` as resulting in the exact same values for the same expressions in all cases. However, `&&` will short-circuit expression evaluation whereas `&` doesn't short-circuit and will evaluate all operands.

### 2. Numbers  
In C#, there is not a single number type but several. For now, lets focus on the most commonly used number types, `int`, `float`, and `double`.

#### Integers
In the number system and in programming, integers represent integral parts of numbers like 1, 578, and 3876545. We cannot represent fractional parts with the `int`eger type.

Let's change our store discount program a little and start calculating discounts for members:
```
var isRetired = true;
var isStoreMember = true;
var shouldApplyDiscount = isRetired && isStoreMember;
// a new variable to hold the purchase amount, note the variable type int
int purchaseAmount = 500;
// below is the amount of discount we want to give our members
int discountAmount = 10; // this means 10% discount on all purchases!

if (shouldApplyDiscount) 
{
    // now we can use our integer variable to calculate discount
    // be careful here, the below may look very strange, how can we use a variable and then assign it back to itself? And what does / mean?!
    purchaseAmount = purchaseAmount - purchaseAmount / 10; // purchaseAmount = 500 - 500 / 10 = 500 - 50 = 450. 
}
```  

This may be a lot to take in, let's understand it.

We need to calculate the discount for a purchase, so the purchase is worth 500 so we need to substract the discount from that. The following line handles that calculation:  
`purchaseAmount = purchaseAmount - purchaseAmount / 10;` 

Breaking this up, we get the following process of how the computer executes our code:
1. Take the value in purchaseAmount and we get: `purchaseAmount = 500 - 500 / 10`
2. Calculate the division of 500 and 10, `/` means divide in programming so we get `500 / 10 = 50`
3. Take the intermediate result of the above division and subtract it from purchaseAmount, our line may look like: `purchaseAmount = 500 - 50` 
4. Calculate `500 - 50` and our line changes to: `purchaseAmount = 450;`
5. Our calculation is complete and the computer concludes by re-assigning the value of `450` o our `purchaseAmount` variable 

It is important to note the order of operations here, divide took preference over the subtraction, if the computer instead did the subtraction first, we'd get a result of `purchaseAmount = 0 / 10` and that's not correct mathematically. And so, programming languages are aware enough to ensure our operations take place in the correct order, this is called `operator precedence`. Briefly, divide `/` has a higher precedence than subtraction `-`, just like in regular arithemetic.

We could have also used parentheses in our program to explicitly describe our desired order of operations: `purchaseAmount = purchaseAmount - purchaseAmount / 10;` is equivalent to `purchaseAmount = purchaseAmount - (purchaseAmount / 10);`. Parentheses tell our program to do give everything inside of it the highest precedence, and is therefore evaluated before anything else.

#### Floating Point Numbers
Integers are certainly useful, but they don't always serve every situation well. To accurately model our store program, we need to be able to represent cents, i.e. fractional parts. That's where floating point numbers come in! The name _floating point_ refers to the dot that separates integral parts form fractional parts. The floating point number `250.99` has an integral part of `250` and a fractional part of `99`.

For now, we'll look at two floating point types `float` and `double`. To make our store program more accurate and realistic with discount calculations we can store our purchase amount as a `float`:

```
var isRetired = true;
var isStoreMember = true;
var shouldApplyDiscount = isRetired && isStoreMember;
// notice our variable type of float
float purchaseAmount = 500.0; 
// below is the amount of discount we want to give our members
int discountAmount = 10; 

if (shouldApplyDiscount) 
{
    // now we can use our float variable to calculate discount
    purchaseAmount = purchaseAmount - purchaseAmount / 10; // purchaseAmount = 500 - 500.0 / 10 = 500 - 50.0 = 450.0 
}
``` 

The order of operations are the same for the previous version of our program with integers, but it is important to note that purchaseAmount is now of type `float` and cannot be anything else. We could have also used the type `double` to represent our purchaseAmount; the only difference between `float` and `double` is that `double` can represent many more numbers than `float` as shown in the _number precision_ section. 

You might wonder why we can divide a floating point number, `500.0`, by an integer, `10`. They're not the same type! We can do this because these number types are compatible as far as arithmetic operations go. When using two number types in a calculation, programming languages will always try and provide you with the most precise type as the result. For instance, `float` is more precise than `int`, but `double` is more precise than both `int` and `float`. Precision usually refers to the range of numbers a particular type can represent.

In our example we are dividing a `float` with an `int`, that means our operation results in a `float`. In our first example we divided an `int` by an `int` which gave us an `int`. For completeness, if did divided a `float` or `int` by a `double`, our operation will result in a `double`. We always get the most precise type present in our calculation back out.

*Beware* of something called _integer division_, this occur when dividing an `int` by another `int` and means we may lose numbers! Take for example `365 / 10`, you'd expect the result to be `36.5` (but that's a `float` type!), our result will in fact be just `36`, our `0.5` is thrust into the ether never to be seen again. This is because programming languages cannot make any assumptions as to what we are trying to achieve and must take the predictable path of always giving us a resultant `int` type when dividing two integers. 

#### Number operations
