# Crash Course on Python - Week 3

In this module you'll explore the intricacies of loops in Python! You'll learn how to use while loops to continuously execute code, as well as how to identify infinite loop errors and how to fix them. You'll also learn to use for loops to iterate over data, and how to use the range() function with for loops. You'll also explore common errors when using for loops and how to fix them.

### Learning Objectives

* Implement while loops to continuously execute code while a condition is true
* Identify and fix infinite loops when using while loops
* Utilize for loops to iterate over a block of code
* Use the range() function to control for loops
* Use nested while and for loops with if statements
* Identify and correct common errors when using loops

---

## While Loops

```
x = 0
while x < 5:
  print("Not there yet, x=" + str(x))
  x = x + 1
print("x=" + str(x))
```
How many times will "Not there yet" be printed?

**5**

Can you work out what this function does? Try passing different parameters to the attempts function to see what it does. 

```
def attempts(n):
    x = 1
    while x <= n:
        print("Attempt " + str(x))
        x += 1
    print("Done")
    
attempts(2)
```
Output:

```
Attempt 1
Attempt 2
Done
```
In this code, there's an initialization problem that's causing our function to behave incorrectly. Can you find the problem and fix it?

**Need to initialize the variable**

```
def count_down(start_number):
  #current = start_number
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)

```
Output:

```
3
2
1
Zero!
```

The following code causes an infinite loop. Can you figure out what’s missing and how to fix it?

**Stopping infinit loop**

```
def print_range(start, end):
	# Loop through the numbers from start to end
	n = start
	while n <= end:
		print(n)
        #n+= 1
print_range(1, 5)  # Should print 1 2 3 4 5 (each number on its own line
```

Output:

```
1
2
3
4
5
```

## For Loops

What is a for loop?
for x in range(5):

  print(x)

Similar to if statements and while loops, for loops begin with the keyword for with a colon at the end of the line. Just like in function definitions, while loops and if statements, the body of the for loop begins on the next line and is indented to the right. But what about the stuff in between the for keyword and the colon? In our example, we’re using the range() function to create a sequence of numbers that our for loop can iterate over. In this case, our variable x points to the current element in the sequence as the for loop iterates over the sequence of numbers. Keep in mind that in Python and many programming languages, a range of numbers will start at 0, and the list of numbers generated will be one less than the provided value. So range(5) will generate a sequence of numbers from 0 to 4, for a total of 5 numbers.

Bringing this all together, the range(5) function will create a sequence of numbers from 0 to 4. Our for loop will iterate over this sequence of numbers, one at a time, making the numbers accessible via the variable x and the code within our loop body will execute for each iteration through the sequence. So for the first loop, x will contain 0, the next loop, 1, and so on until it reaches 4. Once the end of the sequence comes up, the loop will exit and the code will continue.

The power of for loops comes from the fact that it can iterate over a sequence of any kind of data, not just a range of numbers. You can use for loops to iterate over a list of strings, such as usernames or lines in a file.

Not sure whether to use a for loop or a while loop? Remember that a while loop is great for performing an action over 

