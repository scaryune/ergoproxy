# C# delegates

In C#, a delegate is a pointer to a method. That means, a delegate holds the address of a method which can be called using that delegate.

Let's learn how we can define and execute a delegate.

---

## Define a delegate

We define a `delegate` just like we define a normal method. That is, `delegate` also has a return type and parameter. For example,

```
public delegate int myDelegate(int x);
```

Here,

- `delegate` - a keyword
- `int` - return type of delegate
- `myDelegate` - delegate name
- `int x` - parameter that the delegate takes

Any method from any accessible class or struct that matches the delegate signature can be assigned to the delegate.

**Note:** A delegate is also called type-safe pointer.

---

## Instantiate a delegate

Suppose, we have a method named `calculateSum()` whose signature is the same as `myDelegate`.

To create an instance of `myDelegate`, we pass a method name as a parameter. For example,

```
myDelegate d1 = new myDelegate(calculateSum);
```

---

## Example: Calling a Method Using delegate

```
using System;
using System.Collections.Generic;
class Program
{
    // define a method that returns sum of two int numbers 
    static int calculateSum(int x, int y)
    {
        return x + y;
    }

    // define a delegate
    public delegate int myDelegate(int num1, int num2);

    static void Main()
    {
        // create an instance of delegate by passing method name 
        myDelegate d = new myDelegate(calculateSum);

        // calling calculateSum() using delegate
        int result = d(5, 6);

        Console.WriteLine(result);
    }
}
```

**Output**

11

In the above example, we have created an instance of `myDelegate` `d`) and passed `calculateSum()` as a parameter.

Here, we have called the `calculateSum()` method by passing **5** and **6** as parameters values in `d`.

---

## Use of C# delegates

We can use delegates to:

- promote reusability of code and implement flexibility
- notify which method to call when an event is triggered
- define callback methods

---

## Frequently Asked Questions

Multicast Delegate in C#