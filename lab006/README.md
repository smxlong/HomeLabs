# Lab 006: Different Parts of Source Code

### Points: 50

In this lab we will look deeper at the `HelloWorld.java` file you wrote
in the last lab.

This is the program you created:

```java
package lab005;

// This is my first program, HelloWorld
public class HelloWorld {
    // The main function
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

Let's look at what each of these lines of code means.

## package lab005;

Line 1 of the file says `package lab005`. This line is called the "package
statement" and it tells Java what source code package this source file is
a part of. Java is strict about how you name things. The name of the directory
a source code file is in must match the name of the package. Because the source
code of Lab 005 in in a directory called `lab005`, the package name must also
be `lab005`.

## public class HelloWorld {

Line 4 of the file says `public class HelloWorld {`. This line begins a class
definition and it tells Java we are about to write the code for a class called
`HelloWorld`.

What is a class? A class is kind of like a subprogram within a main program.
In Java, all code must be inside a class, so a program must have at least one
class in order to do anything.

The word `public` is called an "access modifier." We will get to that in a
later lab.

At the end of the line is a `{` or "curly brace" character. The curly brace
opens a "block." Blocks are used to group lines of code together.

Notice how the `{` lines up with a matching `}` character at the
very end of the file. Every opening curly brace must match up with a closing
curly brace. To keep track of all these braces, programmers add extra space
at the beginning of lines, called "indenting," to make it easier to see that
a group of lines is inside a block.

## public static void main(String[] args) {

Line 6 of the file says `public static void main(String[] args) {`. Let's break
that apart a little bit.

The `public static void` portion says "This is a method," meaning a piece of
code which is part of the class - instructions for the computer to execute.

The `main` portion is the *name* of the method.

The `(String[] args)` part are the *parameters* of the method. This is data that
is handed to the method when it runs. In this case, we are telling Java that the
method takes a parameter called `args` and that it is an array of `String`. The
meaning of all these terms will be explained later.

Finally, the `{` opens a block (like always). The actual lines of code for the
method are inside this block. The following `}` closes the block.

> Why `main`? When you run a Java class, the computer looks for a method called
> `main` inside the class, then runs that method. In order for your program to
> do anything, it must happen inside the `main` method (or inside some other
> method that is called by the `main` method). In other words, if you put your
> code in a method called `bananas` (for example), it won't run unless you
> call that method from your `main` method. Don't worry if this doesn't
> completely make sense. We'll get to methods calling other methods next.

## System.out.println("Hello, world!");

Line 7 finally contains a "real" line of code! The `main` method contains a
single statement which is: `System.out.println("Hello, world!");`

First, notice that the statement ends with a `;` just like all statements.
You'll need to remember to properly end your Java statements with `;`.

This line of code is a "method call." We are calling (transferring control
of the program to) another method. In this case, the method we are calling
is called `println`. This stands for "print line" and calling it will tell
the computer to print something on the screen.

After `println` is a `(` character: an opening parenthesis. Notice that
there is a matching `)` later on the line. Inside the parentheses is
`"Hello, world!"`. This is called a "string." A sequence of characters
(letters, numbers, or other symbols) inside of double quotes is called a
string in Java (and in most other programming languages).

The `System.out` part of the line tells Java what *object* the method is
being called on. This tells Java, "who is this method being called for?"

For example, suppose there is a method `eat`. When the method is called,
we ask "who is eating?" Different people could be eating. `Katie` could be
eating, or `Jane` could be eating. So in a Java program, we might have a
statement saying `Katie.eat()` meaning Katie should eat, or `Jane.eat()`
meaning Jane should eat. `eat` is the method, `Jane` or `Katie` is the
object.

Here, `System.out` is the name of an object. It is the name of the
*standard output stream* of the program. Anything that is sent to the
standard output stream will be displayed on the screen. Therefore, the
line of code `System.out.println("Hello, world!");` means "Display the
letters `Hello, world!` on the screen."
