# Lab 005: Building a Hello World Java application

### Points: 50

The first program a person writes in a new language is often "Hello World."
A Hello World program just prints the message "Hello, world!" on the screen
and then exits.

## Install the Java extension for VSCode

Before we can work on Java files in VSCode, we need to install an extension.
Extensions are bits of code that add features to VSCode - kind of like mods.

Click on the extensions tab VSCode and type "Java Extension Pack" into the search
box. When it appears in the list, click on it and then click the blue "Install"
button.

Now VSCode has the Java extension installed.

## Create the application

Our program source code is a single file. We'll call it `HelloWorld.java`.

Right click on the `lab005` folder in VSCode and select "New File." Then type the
filename `HelloWorld.java` and press Enter. In programming, the extension of the filename (the
word that occurs after the dot) determines what type of file something is. Java
programs are written in `.java` files.

Now, click on the file you just created. The file contents will appear in the editor,
blank. Enter the following code:

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

Notice that as you type in the code, the text appears in different colors. The colors
make it easy to see the different kinds of words, or "tokens," that the program is made
of. Like human languages, computer languages usually use words arranged in specific
patterns, with spaces in between.

The lines that start with `//` are "comments." Comments are ignored by the computer, but
help the programmer remember what is going on, and tell other people the purpose of the
code after the comment. If you write good comments, you will not have to scratch your
head later when you open up a source code file you haven't worked on in a while and try
to make changes. Write good comments!

Now save the file. You can hit `Ctrl+S` or select Save from the menu.

Once the file is saved, you should see the words `Run | Debug` appear over the line
that says `public static void main`. Click on the word "Run" and look at the bottom
of the screen. You will see the program start up and print the words "Hello, world!"

Congratulations, you wrote your first Java program.
