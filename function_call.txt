Hi Everyone,

In this short video, I want to talk about the anatomy of a function call.  As you've probably heard, most of the code you write in R is nothing more than calls to various functions.  And what is a function?  Well, I'm glad you asked.  

Noted computer science educator John Zelle writes, “You can think of a function as a small program inside a program.  The basic idea of a function is that we write a sequence of statements and give that sequence a name. The instructions can then be executed at any point in the program by referring to the function name.  When a function is subsequently used in a program, we say that the definition is called or invoked.”

So, the best way to illustrate this is to write a function call...

In this case, I'm going call rnorm(), a function that generates a set of random numbers from a normal distribution.  First let's look at the documentation for this function to see what arguments it accepts.  You can do this two ways.

?rnorm or help(rnorm)

From the help documentation, we see that rnorm is one of a family of 4 functions.  It's the last one listed here.  As well, we see that rnorm() takes 3 arguments, sometimes called parameters.  Keep in mind that the term 'argument' and 'parameter' are used interchangeably in the technical literature. 

Okay, let's write some code to call rnorm()...

Because rnorm returns a set of values, we first need to create a variable to hold the results.  Let's call that 'tst'.  Then type the assignment operator, and finally the function name with parenthesis.  Within the parenthesis, we then type each argument with a corresponding value.

tst <- rnorm(n = 100, mean = 2, sd = 1.5)

Now in this piece of code, I'm passing arguments to rnorm by NAME.  That is, I specify the name of the argument, an equal sign, and then a value.  But this code can be written a different way.  Here's another way to call rnorm()...

tst <- rnorm(100, 2, 1.5)

Here I pass the arguments by position.  When doing this, you must ensure that your arguments align with what the function expects at that location.  

And finally, you can call rnorm by NAME and POSITION.  Here's an example of how to do that:

tst <- rnorm(n = 100, 2, 1.5)

In this case, I'm passing the first argument by NAME, the 2nd and 3rd by POSITION.

Although you can call a function in any one of these three ways, my personal preference is to pass arguments to functions by NAME.  When you do that, you know exactly what's being passed to the function.  And your code becomes self-documenting.  This is important when you come back to a piece of code after a period of time.

And with that, we've completed this short video tour of function call anatomy.  

Thank-you for your time.

