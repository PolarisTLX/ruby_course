<!-- This lesson will cover how to output things to the screen in Ruby and how to get input from the user. -->

### Introduction

In this part of the programming fundamentals, we will talk about input & output operations in Ruby. Input is any data that is read by the program, either from a keyboard, file or other programs. Output is data that is produced by the program. The output may go to the screen, to a file or to another program.

Input & output is a large topic. We bring forward some examples to give you a general idea of the subject. Several classes in Ruby have methods for doing input & output operations with the console, files, directories, other programs, or users. In order to learn the basics this lesson will focus on reading and writing to the console.

### Learning Outcomes
*Look through these now and then use them to test yourself after doing the assignment*

what the student is expected to know or be able to do by the end of this lesson

* What is the difference between `print` and `puts`?
* What are the uses for `p`, `printf`, and `putc`?
* How do you get input from the console?

###Ruby writing to console

Ruby has several methods for printing output on the console. These methods are part of the Kernel module. Methods of the Kernel are available to all objects in Ruby. The `print` and `puts` methods produce textual output on the console. The difference between the two is that `puts` adds a new line character. In the example below the two statements are equivalent.

```
print "Apple\n"
puts "Orange"
```

The `print` method prints to the console on the same line. If we want to create a new line, we must explicitly include a newline character like the example above. The newline character is \n.

Ruby has another three methods for printing output to the console. The `p` calls the `inspect` method upon the object being printed. This method is useful for debugging. The `printf` method is well known from the C programming language. It enables string formatting. The `putc` method prints one character to the console. These three examples are less common but it is nice to know they exist.

```
p "Lemon"
printf "There are %d apples\n", 3
putc 'K'
```

###Ruby reading input from console

The common way to read data from the console is to use the `gets` method. Take a look at the example below. We use the `gets` method to read a line from the user. The data is assigned to the name variable. Then the data that we have read is printed to the console with `puts`. We use interpolation to include the variable in the string.

```
print "Enter your name: "
name = gets
puts "Hello #{name}"
```

In the script above, if we call the `size` method on a name with 4 characters like “Ruby”, the method would return 5. The `size` method counts the new line character \n that is included when you press enter in the terminal. We will need the `chomp` method. It is a string method which removes white spaces from the end of the string. To have `size` return a length of 4, we need to remove the newline character. This is a job for the `chomp` method.

```
print "Enter a string: "
input = gets.chomp
puts "The string has #{input.size} characters"
```

### Assignment

* If you haven't done so already, complete the first lesson of learn ruby from Codecademy [Learn-Ruby](https://www.codecademy.com/learn/learn-ruby).

### Additional Resources
*This section contains helpful links to other content. It isn't required, so consider it supplemental for if you need to dive deeper into something*

* Read the chapter on input and output [here](http://ruby.bastardsbook.com/chapters/io/).
