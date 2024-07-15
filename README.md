/// Exercise 5.5 
/// Problem 1. Draw a stack diagram showing the state of the program just before the last instance of Prod completes. What is the output?
/// A: Prod(1,4) calls Prod(1,3)
/// A: Prod(1,3) calls Prod(1,2)
/// A: Prod(1,2) calls Prod(1,1)
/// A: Prod(1,1) returns 1
/// A: Prod(1,2) can then return 2
/// A: Prod(1,3) can then return 6
/// A: Prod(1,4) can then return 24 - the final function call

/// Problem 2. Explain in a few words what Prod does.
/// A: This is a recursive program that takes 2 integer inputs 'm' and 'n'.
/// A: It assumes that 'm' is less than 'n', as it decrements by 1 if they are not equal.
/// A: The program iterates Prod until m == n, and then the program prints 'n'.
/// A: Once it prints 'n', it can then print 'result' as it now has a definite value for 'recurse'.
/// A: The final output is an ascending list of numbers that totals up to 24.

/// Problem 3. Rewrite Prod without using 'recurse' and 'result'
/// A: Prod2 uses the same IF/ELSE structure but the ELSE returns 'n * Prod2(m, n-1)'.
/// A: I am impressed that the function could return a call to another function.

/// Problem 5.7
/// Lines 11-21 on Main() run test outputs for their programs

/// Problem 6.2
/// 1. Why does it not stop when COUNT reaches 1.0?
/// A: Floating-point arithmetic can be imprecise when done by a computer due to
/// A: unseen rounding errors in the background. It may never ever equal 1.0 unless
/// A: explicit measures are implemented to reduce these errors to near-zero.
/// 
/// 2. How can you alter it to do so?
/// A: Change the WHILE loop statement as follows:
/// A: while(Maths.Abs(count - 1.0) > 0.0000001)
/// A: The rounding differences within a computer can be as small as 2.22(10^(-16))
/// A: but this ensures that "1.0 - 1.0" catches the proximity COUNT to the break
/// A: condition.

/// Problem 6.3
/// The process of creating a double[] array to compare value(n) against 
/// value(n-1) became cumbersome and unnecessary. Rather than store all values,
/// I decided to cycle the current and previous values until the acceptable product
/// broke the while loop.

/// Problem 7.5
/// 1. What happens when you add a string to a char?
/// A: It concatenates the string with the char, which is converted into a string.
/// A: The resulting type can be accessed with GetType(result).
/// 
/// 2. Describe what happens at the '+' intersection between the following types?
/// A: bool + bool cannot be added together
/// A: Booleans are incompatible with any other type
/// A: Chars can be concatenated with strings, and they convert to Unicode when added with INT
/// A: Strings are extremely flexible in that they convert BOOL to their value before 
/// A: incorporatig them as strings. Same with CHAR and INT.
/// 
/// 3a. How many seem unavoidable?
/// A. The relationship between BOOL values and CHAR / INT seems like the only choice.
/// 
/// 3b. How many seem like a reasonable choice picked from a pool of reasonable choices?
/// A. I'm fond of the versatility of STRING types. Integrating BOOL values makes presentation
/// A. intuitive and easy. I also enjoy how CHAR and INT are converted to STRING.
/// 
/// 3c. How many seem like problematic choices?
/// A. Converting CHAR + CHAR and CHAR + INT into Unicode seems very problematic and counterintuitive.
/// A. It would be much better to convert those intersections into STRING type.# CS205-Week2
