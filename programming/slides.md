---
marp: true
theme: uncover
author: Joshua Bas
math: katex
---

# **Programming Layer**

AP CSP @ SouthLake Christian Academy

---

## Basic Terminology

* A program is a collection of program statements that performs a specific task when run by a computer. A program is often referred to as software.
* A code segment is a collection of program statements that is part of a program.

<!-- often called program behavior -->

**Program function is how softare accomplishes a task**
**Program purpose is why software accomplishes a task**

---

We will be programming in Python

* Python files end in `.py`
* Python allows for programs to work basically the same on any machine

---

## **Pseudocode**

* **pseudocode**: "false code" &rarr; an informal tool that uses English to represent a set of *strict* instructions

<pre>
0. Do first step
1. Do second step
2. Do next step...
</pre>

---

### Pseudocode for: Brushing Teeth

---

---

* We have instructions that occur in *sequence*
* Some of these lines start with verbs, or actions. We'll start calling these *functions* or *procedures*
* We also have questions that lead to different paths, like forks in the road, which we'll call *conditions*:
* And the answers to questions that decide where we go are called *Boolean expressions*, which eventually result to a value of true or false
* Finally, we have words that lead to cycles, where we can repeat parts of our program, called *loops* or *iterations*:

---

## **Flowcharts**

Another useful tool for visualizing a set of instructions

![width:400px](https://github.com/APCSP-SLCA/apcsp-slca.github.io/raw/gh-pages-dev/assets/images/flowchart_example.png)

---

## **Comments**

are not part of the program; the Python interpreter will completely ignore lines that start with `#` or text enclosed in `"""`

<pre>
<samp>
    """
    This text is ignored. Use comments to describe your program!

    I can write multi-line comments!
    """

    # This line is also ignored
</samp>
</pre>

---

## **Variables**

a *variable* is a piece of memory that holds some value
NOTE: x = 1 means "assign x the value of 1" NOT "x equals 1"

---

### Variable Operations

| Operator | Example |
|----------|---------|
| +        | y = x + 1   |
| -        | y = x - 1 |
| *        | y = x * 2 |
| **        | y = x ** 2 |
| /       | y = x / 2 |
| //        | y = x // 2 |
| %         | y = x % 10 |

---

### `print`

displays content to console

<pre>
<samp>
    print("Hello, World!")
    >> Hello, World!
    >>
</samp>
</pre>

specify the line ending with end:

<pre>
<samp>
    print("Hello, World!", end="a")
    >> Hello, World!a
</samp>
</pre>

---

`\n` is a special character that specifies newlines
`\t` is a special character that specifies tabs

by default, `end="\n"`

---

### `input`

asks the user for some input, returns a string of characters

will wait until user types something and presses Enter/Return

<pre>
<samp>
    x = input("What is your name?")
</samp>
</pre>

---

## **Functions**

abstractions that allow us to group related code statements

<pre>
<samp>
    def myFunction():
        print("Yay")
</samp>
</pre>

---

### Arguments and Returns

*parameters* or *arguments* are inputs to functions

<pre>
<samp>
    def myFunction(msg):
        print("I was given:")
        print(msg)
</samp>
</pre>

a function can *return* a value to the function caller:
<pre>
<samp>
    def addOne(x):
        return x + 1
</samp>
</pre>