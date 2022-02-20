# 2. Expressions, Variables and Constants

1.  **Comments**:

    Swift, like most other programming languages, allows you to document your code through the use of what are called **comments**. These allow you to write any text directly alongside your code and are ignored by the compiler.

    ```
    1\. Single line Comment
    // This is a comment. It is not executed.

    2. Multi-line Comment

    	2.a
    /* This is also a comment.
       Over many..
       many...
       many lines. */

    	2.b
    /* This is a comment.

     /* And inside it
     is
     another comment.
     */

     Back to the first.
     */

    ```

2.  ****Printing out:****

    In Swift, you can achieve this through the use of the `print` command. `print` will output whatever you want to the **debug area** (sometimes referred to as the console).

3.  ****Arithmetic operations:****

    When you take one or more pieces of data and turn them into another piece of data, this is known as an **operation**.

    Swift uses the following operators:

    -   Add: `+`
    -   Subtract: ``
    -   Multiply: ``
    -   Divide: `/`

    **Remainder:** This operation, also called the modulo operation. In division, the denominator goes into the numerator a whole number of times, plus a remainder. This remainder is exactly what the remainder operation gives.

    If you want to compute the same thing using decimal numbers, you do it like so:

    ```
    (28.0).truncatingRemainder(dividingBy: 10.0)

    ```

    ****Shift operations:****

    The **shift left** and **shift right** operations take the binary form of a decimal number and shift the digits left or right, respectively. Then they return the decimal form of the new binary number.

    The operators for these two operations are as follows:

    -   Shift left: `<<`
    -   Shift right: `>>`

    One reason for using shifts is to make multiplying or dividing by powers of two easy. Notice that shifting left by one is the same as multiplying by two, shifting left by two is the same as multiplying by four, and so on.

    Likewise, shifting right by one is the same as dividing by two, shifting right by two is the same as dividing by four, and so on.

    ****Order of operations:****

    ```
    ((8000 / (5 * 10)) - 32) >> (29 % 5)

    ```

    Swift uses the same reasoning and achieves this through what's known as **operator precedence**. The division operator (`/`) has higher precedence than the addition operator (`+`), so in this example, the code executes the division operation first.

    ****Math functions:****

    ```
    sin(45 * Double.pi / 180)
    // 0.7071067811865475

    cos(135 * Double.pi / 180)
    // -0.7071067811865475

    ```

    These convert an angle from degrees to radians and then compute the sine and cosine, respectively. Notice how both make use of `Double.pi`, which is a constant Swift provides us, ready-made with pi to as much precision as is possible by the computer. Neat!

    Some more examples:

    ```
    (2.0).squareRoot()
    // 1.414213562373095

    max(5, 10)
    // 10

    min(-5, -10)
    // -10

    ```

4.  ****Naming data:****

    In your Swift code, you can give each piece of data a name you can refer to later. The name carries with it a **type annotation** that denotes what sort of data the name refers to, such as text, numbers, or a date.

    1.  ****Constants:****

        ```
        let number: Int = 10          // Constant of type : Int
        let pi: Double = 3.14159      // Constant of type : Double

        ```

        `Double`, a type that can store decimals with high precision.

        There's also a type called `Float`, short for floating-point, that stores decimals with lower precision than `Double`. In fact, `Double` has about double the precision of `Float`, which is why it's called `Double` in the first place

    2.  ****Variables:****

        When you know you'll need to change some data, you should use a variable to represent that data instead of a constant. You declare a variable in a similar way, like so:

        ```
        var variableNumber: Int = 42

        ```

        In Swift, you can even use the full range of Unicode characters. For example, you could declare a variable like so:

        ```
        var 🐶💩: Int = -1

        ```

    3.  **Increment and Decrement:**

        ```
        var counter: Int = 0

        counter += 1
        // counter = 1

        counter -= 1
        // counter = 0

        ```

        The `counter` variable begins as `0`. The increment sets its value to `1`, and then the decrement sets its value back to `0`.
