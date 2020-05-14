# Lab 008: Calling methods

### Points: 50

In the program you just wrote for Lab 007, your program printed the
message `Hello, world!` twice.

When you want your code to do the same thing more than once, you don't
have to type out the same code again. Instead, you can put the code in
a method, and then "call" that method from somewhere else.

The output from Lab 007 looks like this:

```
Hello, world!
Welcome to Lab007
Hello, world!
The next lab is Lab008
```

And your code probably looks something like this:

```java
package lab007;

// This is my first program, HelloWorld
public class HelloWorld {
    // The main function
    public static void main(String[] args) {
        System.out.println("Hello, world!");
        System.out.println("Welcome to Lab007");
        System.out.println("Hello, world!");
        System.out.println("The next lab is Lab008");
    }
}
```
## Make a copy

1. Copy your Lab 007 program into the `lab008` directory.
2. Rename the `package` to `lab008`.
3. Update the messages to say `Welcome to Lab008` and
   `The next lab is Lab009`.

## Writing a method

Now we are going to add a new method to print `Hello, world!` and use that
from our `main` method instead of printing the message directly.

Add this method to your program, inside the curly braces of the `class`:

```java
public static void printHelloWorld() {
    System.out.println("Hello, world!");
}
```

## Calling a method

Now, replace the lines of code in your `main` method that print `Hello, world!`
with lines that call the new method you've just written. When you're done, your
program should look like this:

```java
package lab008;

// This is my first program, HelloWorld
public class HelloWorld {
    // The main function
    public static void main(String[] args) {
        printHelloWorld();
        System.out.println("Welcome to Lab008");
        printHelloWorld();
        System.out.println("The next lab is Lab009");
    }

    public static void printHelloWorld() {
        System.out.println("Hello, world!");
    }
}
```

## Commenting your code

Remember our conversation about comments? Let's add a comment to our new method
that reminds us what it's for:

```java
// printHelloWorld prints our welcome message
public static void printHelloWorld() {
    System.out.println("Hello, world!");
}
```

## Test the code

Now run the code and make sure you see the correct output. The output should still
look like this:

```
Hello, world!
Welcome to Lab008
Hello, world!
The next lab is Lab009
```

## Updating the method

Now let's show the power of methods by changing the code inside the method and
seeing that what our program does also changes everywhere that method is called.

Edit your `printHelloWorld` method to print the message `Welcome to HomeLabs!`.
Run your program again, and notice that *both* copies of the message have been
changed. The final output of your program should look like this:

```
Welcome to HomeLabs!
Welcome to Lab008
Welcome to HomeLabs!
The next lab is Lab009
```
