---
marp: true
theme: uncover
author: Joshua Bas
math: katex
---

# **Programming Layer**

AP CSP @ SouthLake Christian Academy

---

## **Pseudocode**

* **pseudocode**: "false code" &rarr; an informal tool that uses English to represent a set of *strict* instructions

<pre>
0. Do first step
1. Do second step
2. Do next step...
</pre>

---

### Pseucode for: Brushing Teeth

---

---

### Pseucode for: Using a Phonebook

We have instructions that occur in *sequence*:
<pre>
0 pick up phone book
1 open to middle of phone book
2 look at names
3 if Smith is among names
4     call Mike
5 else if Smith is earlier in book
6     open to middle of left half of book
7     go back to step 2
8 else if Smith is later in book
9     open to middle of right half of book
10    go back to step 2
11 else
12     quit
</pre>

---

Some of these lines start with verbs, or actions. We'll start calling these *functions* or *procedures*:
<pre>
0 <b>pick up</b> phone book
1 <b>open to</b> middle of phone book
2 <b>look at</b> names
3 if Smith is among names
4     <b>call</b> Mike
5 else if Smith is earlier in book
6     <b>open to</b> middle of left half of book
7     go back to step 2
8 else if Smith is later in book
9     <b>open to</b> middle of right half of book
10    go back to step 2
11 else
12     <b>quit</b>
</pre>

---

We also have questions that lead to different paths, like forks in the road, which we'll call *conditions*:
<pre>
0 pick up phone book
1 open to middle of phone book
2 look at names
3 <b>if</b> Smith is among names
4     call Mike
5 <b>else if</b> Smith is earlier in book
6     open to middle of left half of book
7     go back to step 2
8 <b>else if</b> Smith is later in book
9     open to middle of right half of book
10    go back to step 2
11 <b>else</b>
12     quit
</pre>

---

And the answers to questions that decide where we go are called *Boolean expressions*, which eventually result to a value of true or false:
<pre>
0 pick up phone book
1 open to middle of phone book
2 look at names
3 if <b>Smith is among names</b>
4     call Mike
5 else if <b>Smith is earlier in book</b>
6     open to middle of left half of book
7     go back to step 2
8 else if <b>Smith is later in book</b>
9     open to middle of right half of book
10    go back to step 2
11 else
12     quit
</pre>

---

Finally, we have words that lead to cycles, where we can repeat parts of our program, called *loops* or *iterations*:
<pre>
0 pick up phone book
1 open to middle of phone book
2 look at names
3 if Smith is among names
4     call Mike
5 else if Smith is earlier in book
6     open to middle of left half of book
7     <b>go back to step 2</b>
8 else if Smith is later in book
9     open to middle of right half of book
10     <b>go back to step 2</b>
11 else
12     quit
</pre>