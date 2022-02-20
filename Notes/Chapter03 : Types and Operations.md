3\. Types & Operations
======================

Formally, a **type** describes a set of values and the operations that can be performed on them.

1.  ****Type conversion:****

    Sometimes you'll have data in one format and need to convert it to another. In Swift, that includes being explicit about type conversions. If you want the conversion to happen, you have to say so!

    Instead of simply assigning, you need to say that you want to convert the type explicitly. You do it like so:

    ```
    integer = Int(decimal)

    ```

2.  ****Type inference:****

    It turns out the Swift compiler can deduce this as well. It doesn't need you to tell it the type all the time --- it can figure it out on its own. This is done through a process called **type inference**. Not all programming languages have this, but Swift does, and it's a key component of Swift's power as a language.

    Sometimes it's useful to check the inferred type of a variable or constant. You can do this in a playground by holding down the **Option** key and clicking on the variable or constant's name. Xcode will display a popover like this:

    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f609bae-4dec-472c-a665-5fc9387e45c4/Untitled.png)

    ```
    let wantADouble = 3

    ```

    Here, Swift infers the type of `wantADouble` as `Int`. But what if you wanted `Double`instead?

    The first thing you could do is the following:

    ```
    let actuallyDouble = Double(3)

    ```

    This is like you saw before with type conversion.

    Another option would be to not use type inference at all and do the following:

    ```
    let actuallyDouble: Double = 3

    ```

    There is a third option, like so:

    ```
    let actuallyDouble = 3 as Double

    ```

    This uses a new keyword you haven't seen before, `as`. It also performs a type conversion, and you'll see it again later in this book.

    > Note: Literal values like 3 don't have a type, and it's only when using them in an expression or assigning them to a constant or variable that Swift infers a type for them.

    > A literal number value that doesn't contain a decimal point can be used as an Intas well as a Double. This is why you're allowed to assign the value 3 to constant actuallyDouble.
    >
    > Literal number values that ***do*** contain a decimal point cannot be integers. This means we could have avoided this entire discussion had we started with:
    >
    > `let wantADouble = 3.0`
    >
    > Sorry! :]

    [Mini-exercise : Ch02](https://www.notion.so/Mini-exercise-Ch02-c7ce1f39aeb14324ac2ca6acb6797517)
