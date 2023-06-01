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
