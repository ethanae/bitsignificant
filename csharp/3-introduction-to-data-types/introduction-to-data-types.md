# BitSignificant CSharp

## 3. An Introduction to Data Types

### Data types form an integral part of statically-typed language such as C#. For now, we are going to explore some types provided to us by the language itself. These types are called primitive data types because they are the usually the most basic types.

### We're going to look at the type listed below:
- `boolean`
- `int`
- `double`
- `float`
- `boolean`
- `char`
- `string`

### 1. Boolean 
A boolean type refers to the values `true` and `false` only. This type gives us the ability to model true/false cases in our code. As you saw in our previous example we saw the declaration of a variable called `isRetired`, we could use this variable to test determine if a user is a pensioner and then discount to some item they want to purchase.  

We can use the boolean value like this:
```
if (isRetired) {
    // some code to apply our discount
} else {

}
```

We've used an _if-else-statement_ here which tests the value of a boolean type. 

#### Boolean operations
As we saw above an _if-else-statement_ can be used to test a boolean value but we can form much more complex expressions with boolean types.

Let's introduce another variable called `isStoreMember` which tells us if a customer is the member of our imaginary store and we want to give customers discount if they're pensioners AND (`&&`) they're a member at our store. Our program might look like:   
```
var isRetired = true;
var isStoreMember = true;
var shouldApplyDiscount = isRetired && isStoreMember;

if (shouldApplyDiscount) {
    // some code to apply our discount
}
```  
Here we are using a new-looking symbol, the double ampersand, `&&`. When we use this syntax we are creating an expression, in this case a boolean expression. You should read `&&` as "AND", which means that both values on either side of the double ampersand should be `true` for the whole expression to be true.

Note that we also get a single ampersand operator, `&`. Firstly, remember that `&&` needs to both values on either side to be true which means if the first operand is `false` we already know that the rest of expression cannot possibly be true because we've already encountered a false value meaning that we don not need to even evaluate the rest of remaining expression. In a sense, `&&` short-circuits expression evaluation. 
  
The `&` operator works a little differently, in that it will always evaluate all operands of our expression but the end value remains the same as `&&`. So if either operand is false, our whole expression with be `false` otherwise all operands are `true` and our whole expression is `true`.

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