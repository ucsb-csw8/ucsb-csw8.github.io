---
layout: home
title: 📝&nbsp;&nbsp; Lab to Code
parent: References
nav_order: 4
seo:
  type: Reference
  name: A guide for how to translate lab instructions to code
---

# 📝 Translating lab instructions to code

Dear all,

Starting this week, labs instructions will be providing you with the specifications for the **functions** to implement as well as giving you guidelines on what to include as part of **your program**.  

**The program** (sometimes referred to as  "_your program_" or the "_main program_") usually needs to use, i.e. _call_, the functions that you _defined_ at the start of the file (using the `def` keyword). 

If your function has one or more _parameter_, then you will need to call the `input()` function _inside of your main program_: the values that you get from the user are going to be passed as _arguments_ from your program into the function through a _function call_.
> This is very important: the _function arguments_ are a way that we tell the _function_ what _specific values_ to use inside the function instead of the _generic parameters_ that we defined. These _arguments_ are provided **during the _function call_** and are substituted for the function _parameters_.

---

## Sample Lab Instructions

Let's deconstruct a sample lab:

---
> ### Learning objectives
> In this lab, you will:
> * define and write the requested function with the specified number of parameters
> * write a program that asks for the user input and converts it into the appropriate type
> * use the collected input when calling the function
> * format the printing of the result (using the `f-string`) to keep your output to two decimal places

> ### Instructions
>  An Olympic-size swimming pool is used in the Olympic Games, where the race course is 50 meters (164.0 ft) in length.
>  In swimming, a lap is one length in distance. By definition, a lap means a complete trip around a race track, in swimming, the pool is the race track. Therefore if you swim from one end to the other, you’ve completed the track and thus you’ve completed one lap or one length. (Source: [What Is A Lap In Swimming? Lap Vs Length](https://swimcompetitive.com/swimming-guides/what-is-a-lap-in-swimming))

>  Write the function `meters_to_laps()` that takes a number of meters as an argument and returns the number of laps. 

> Complete the program to output the number of laps. Output each floating-point value with two digits after the decimal point, which can be achieved as follows: 
```py
print(f'{your_value:.2f}')
```

> ### Test your code
> If the input is:
```
150
```
> the output is:
```
3.00
```

> If the input is:
```
80
```
> the output is:
```
1.60
```
> To clarify, you must first define the following _function_:
> ```def meters_to_laps()``` that takes in length (a floating-point argument representing the distance in meters) and returns the number of laps this distance corresponds to (also a float, since we are formatting the output to two decimal spaces). 
> Then, in your _main program_, you are supposed to take user input and call the function with these values, and print the results with the specified precision.

> _Hint: remember how to convert user input to a floating-point number?_

---
---
---

## Reading through the lab

The start of the lab typically outlines our learning objectives, which are the goals/concepts that we are practicing in this lab. 
It is intended to help you locate those concepts in the book (re-read or reference them before / as you are solving the lab).

🌟 **All labs assume that you are following the suggested [Problem-solving Workflow]({{ site.url }}{{ site.baseurl }}/success#problem-solving-workflow) guidelines that we ask for you to use.** (Make sure to arrange your windows to make it easier for you to keep track of the instructions and your solution.)

The lab might have some introduction to explain the context for the problem and to provide important information. 
In this example, the intro defines a lap and tells us about the length of the race course, which is the value that we will need to use in our solution.
Usually, you _need to read_ the first part of the instructions (intro) in order to know how to solve the problem and write the body of the function. 
* Pause.
* Read and follow **_all_** instructions carefully.
* Manually work through the example and the test input/output to verify that you understand what is being asked _conceptually_.
* As described in the [Problem-solving Workflow]({{ site.url }}{{ site.baseurl }}/success#problem-solving-workflow), develop the pseudocode of the solution, before proceeding.
* Re-read the lab to verify that you solution addresses all provided instructions.

As you can see, the instructions are asking us to
1. define the requested function
1. write a program that calls the function

 Let's take a closer look at these two distinct parts of your code. 

## Function vs. program

🔑 Notice that there are two parts in the _lab solution file_ that you'll need to replace with your code:
* **Function specification**: marked with `''' Define your function here '''`
* **The program**: marked with the `if __name__ == "__main__":` block and `''' Type your code here. Your code must call the function. '''`

### Function specification

📄 **Function specification** will need to be implemented inside the definition that starts with `def`. 

The lab instructions give you the information that you need for the function stub:
> ... the function `meters_to_laps()` ...
> * takes a number of meters as **an argument** and
> * `return`s the number of laps.

Just from these instructions we can get the following function elements:
* the function name
* the name and number of arguments
* the docstring (function documentation)
* the return value

We can copy/paste our skeleton function template and begin updating its components:
```py
def ___( _ ):
    """ 
    This function takes as an argument
    param: meaning/description (type)
    ...
    The function returns/prints object (type).
    """
    # function body
    return _ # or print (check instructions)
```

The code could roughly be as follows (we'll leave the naming of the argument up to you and will replace it with the [ellipsis]({{ site.url }}{{ site.baseurl }}/ref/keyboard#-other-symbols):
```py
def meters_to_laps(...):
    """ The function takes as input
        param: ... - number of meters (float).
        Uses the race course distance of 50 meters (164.0 ft) in length.
        The function returns the number of laps (float).
    """
    ### compute the number of laps
    num_laps = ...
    return num_laps
```

_Note that we can add the types of the arguments in the function docstring by looking at how to test our function and what the output should be._

### The main program

📄 **The program** (i.e., "your program" or "main program") will need to get the user input and call the function to produce the requested output.
The main program has to be implemented _inside_ the `if __name__ == "__main__":` block. 
All lines that are _inside_ the block are indented underneath that line. 
If a line is not indented and is on the same indentation level as the `if __name__ == "__main__":`, then that line is _outside_ of the block.

Your code in this block **must** call the function that you defined _above it_ (remember: only the _function definitions_ and `import` statements should be placed outside of this block).

In the lab instructions, after we implemented the function, we are supposed to:
> Complete the program to
> * output the number of laps.
> * Output each floating-point value with two digits after the decimal point...

After following the lab instructions, for this lab, the structure of the solution could be as follows:

```py
def meters_to_laps(...):
    """ The function takes as input
        param: ... - number of meters (float)
        The function returns the number of laps (float).
    """
    ### compute the number of laps
    num_laps = ...
    return num_laps

if __name__ == "__main__":
   # Get the input from the user
   ...

   # Output each floating-point value with two digits after the decimal point
   num_laps = meters_to_laps(...)
   print('{num_laps:.2f}')
```

## Code template
In general, your code should follow the template shown below.

You can copy/paste the template below, just remember to update the comments.
```py
def function_name(param1, param2, ...):
    """ 
    This function takes as an argument
    param: param1 -  meaning/description (type)
    param: param2 -  meaning/description (type)
    Quick description of the function goal.
    The function returns/prints object (type).
    """

    result = ... # some calculation here to get the final result
    # check the instructions if you need to print something
    return result # remember the return :)  

if __name__ == "__main__":
    var = input() # reading as many inputs as we need
    # program body - see the instructions
    func_result = function_name(var, ..) # a function call, remember to store the result!
    print("This is the final output", func_result) # see instructions for output
    print(f"This is the final output {func_result:.2f}") # some cool format for floats :)

```

## Important notes
📌 A few things to notice:
* Since the instructions didn't ask to `print` anything _within the function_, the definition should **not** include a `print`. 
    * That's not always the case, because sometimes we need to do both (i.e., `print` **and** `return` something) -- **the _instructions_ will specify exactly what you need to do**, so you don't need to guess, just read and follow the instructions.
* If you remove the entire `if __name__ == "__main__"` block, your function should still work by itself.
   * Your functions should NOT rely on variables that are outside of the function definition  (e.g., global variables, which are outside of the `def` block, or variables that are inside the `if __name__` block).
   * If you listed parameter names in the function signature, which you are not using inside of your function body, then re-read the previous bullet point and the lab instructions (ask yourself: _"why does my function have a parameter that I haven't used inside the function?"_).
* You _need to read_ the first part of the instructions (intro) in order to know how to solve the problem and write the body of the function. Read and follow **_all_** instructions carefully.

We hope that this is helpful 👍. If you have any follow-up questions 🧐 or comments, we look forward to addressing them on the forum.

Have a productive week!

---
#### Acknowledgements
The lab instructions are based on a sample zyBooks lab.
{: .fs-3 }
Specials thanks to Liubov Kurafeeva for contributing the initial code template.
{: .fs-3 }

