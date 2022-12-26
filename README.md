# python-to-java

Welp, we did it. We managed to get through the hellscape that was 1501 Python. We learned a lot along the way, but the real programming was the friends we made along the way. 1502 looks to be it's own beast, so we should probably get our bases covered early. CS people, sucks to suck, no c++ guide for you. Seethe.

⚠️DISCLAIMER⚠️ I am very sick while writing this so don't blame me if there's a typo or two. Just DM me and I'll fix 'em.

## Installing A JRE

In order to actually "Do a Java", you're gonna need a JRE, or a Java Runtime Environment. This is a little home in your computer where Java is gonna live and do all its work.

1. Go [here](https://www.oracle.com/java/technologies/downloads/#jdk19-windows) and download the `x64 Installer`, unless you're smarter than me and your PC needs a different one. You'll know.

2. If it says 1Do you want to reinstall this?1 like it did to me because I blew past the instructions way too fast and forgot to write this document, just reinstall it.

3. Hit next and next, then close.

## Installing The World's Shittiest Editor (on Windows).

From what I understand, we're gonna be using Eclipse for 1502, which sucks. There's a whole new "perspective" for debugging, the menus are suuuper bloated with crap you're never gonna touch, there are a bunch of VSCode features that you're gonna miss, it's super memory intensive (runs very slow), the default keybinds all suck, the autocomplete is complete garbage, and worst of all: it's light mode by **default**! Ugh!

_anyways here's how you install it:_

1. Grab your nearest pillow, bury your face in it, and let out a hearty scream. Now we can begin.

2. Head over to [Eclipse's website](https://www.eclipse.org/downloads/) and hit the 1Get Eclipse IDE 2022-121 button. The numbers might be a bit different, but you don't care.

3. Hit download, then laugh at the "plz donate" window and promptly close it.

4. Run your newly downloaded .exe file, and select `Eclipse IDE for Jave Developers` cause that's what you are now.

5. This is where you're gonna want to set your installation directory. This is scary, so I left the defaults. Make sure to uncheck the Start Menu and Desktop shortcut buttons, cause those are gross.

6. Hit the big yellow download button, and make sure to skip the Terms and Agreements as fast as possible, because we don't care.

7. You can now hit the big green `Start` button, and watch the world's ugliest boot up screen.

8. Keep your workspace environment as the default, and check the `use default` button. This is where Eclipse is gonna shove all your plugins and configuration files. Hit `Launch`.

9. This is the most important step. Before you do **anything** else, navigate to `Window > Preferences > General`, and under the `Appearance` tab, set your theme to `Dark`. Hit the button that says `Apply`, and then press `Apply and Close`.

10. Restart your computer. This will make sure Java is nicely settled into all the crannies of your PC :)) It lives in there now.

## You are Sisyphus, and Java is your boulder

Let's rock and roll. First, we'll `Create a new Java Project`, and name it something really cool like "LearningToDoAJava". We're gonna write this in **PascalCase**, since that's the standard for Java project names. It **should**, by default, select `JavaSE-17` as your `Execution Environment JRE`, and that's good, we want that. If there's something weird in that box, then Google it idk Java's scary. Uncheck the `Create module-info.java` box, because I really do not feel like explaining Java modules while sick. Finish.

There's gonna be a lot of things on the screen, and it's gonna be really scary, but take a deep breath and we'll work through this. On the right is the `Outline`, which we do not care about. There's a little horizontal rectangle near the top right of that, click that and it'll disappear. At the bottom is the `Problems` box, which will be full very soon, so we can keep that open. Finally, on the left, we got the `Package Explorer`, which is just the VSCode sidebar with extra steps, so don't worry.

Let's write some code already! In your explorer, right click on `LearningToDoAJava`, and under `New`, select `Package`. Let's call it `mypackage`, just for funsies. No checking the `Create package-info.java` box, don't do it. We like to keep the package names in all lowercase in Java, so do that. Hit finish. Your file structure should look something like this:

```
LearningToDoAJava
    JRE System Library [JavaSE-17]
    src
        mypackage
```

Yippee! That's what we want. Alright, let's write some code. Right click on your brand-spankin-new package, and add a new `Class`. We'll name it `MyClass` (PascalCase again), and ensure that `public` and `none` are the only things checked under `Modifiers`. Make sure to check that `public static void main(String[] args)`, or you're gonna have to write it in manually. Leave everything else default, and hit Finish.

```java
package mypackage;

public class MyClass {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

}
```

## Deciphering Whatever That Was

Hey hey! That looks like some Java code! Let's break it down line by line.

That `package mypackage;` is just telling your code what "folder" it's in. We like to put Java classes together in packages, to make them easier to manage. Notice how we end with a semicolon? Get used to it. Whenever we have a line of code that doesn't end in a curly bracket (we'll talk about it), we need a semicolon.

Next up, we got `public class MyClass {`. Remember when we defined classes in Python? Same deal, but with a few more steps. First, we need to tell Java that this class is `public`, which means when we write other code, it'll be allowed to access this class. `class` tells us we're about to define a new class, and `MyClass` is the name of our class! Remember that PascalCase! We also have an opening curly bracket, which is gonna be a whole new world for a lot of you. Where we used to have colons and indents in Python, we now use curly brackets!

Next, we have our `public static void main(String[] args)`. Remember how we'd create a `main()` function in Python? Same thing. We also don't need to call this function on our own like we did in Python, as Java will do that for us. Also, you see how we're working in a class? This means this function is actually a method!

The `public` tells the world that they're totally allowed to call this method.

The `static` is a little confusing, so just tell yourself "it's for memory management" and move on.

The `void` just means this function doesn't return anything! Remember when we used to do `def myfunc() -> None:` in Python? We now call that `None` `Void`, and put it near the start. If we wanted to return a whole number, we'd change it to `int`. A bool? `bool`! It's also no longer optional, so don't forget it!

`main` is the name of our method. We like to use **camelCase** for methods, so keep that in mind.

The parameter that `main` is asking for is an `Array` of `String`s called `args`, which stands for arguments. An `Array` is similar to a `List` in Python, but it is immutable, which means we can't add or remove things from it. Also, you'll notice `String` is capitalized, because it's an object! It's also a datatype, which is why it comes before the parameter name. Remember in Python when we'd use `def myfunc(args: list)`? Instead of putting the expected datatype at the end of the variable name we put it at the beginning! We also gotta specify a bit more, which is why we add those square brackets in front of `String`. That's not only saying "hey, this is a list", but it's telling us it's a list of **only strings**. No more mixing datatypes in `Lists` or `Arrays`, you have to choose one from now on.

## Some Easy Stuff

Ugh, that was a lot. Let's get back to something familiar.

```py
def get_some_input() -> int:
    number = int(input("Please give me a whole number!"))
    return number

def do_some_math(num1: int, num2: int) -> int:
    new_num = 0
    num1 = num1 * num2
    new_num = num1 + 5
    num2 += 1
    num1 -= 1
    return new_num - num1 + num2

def main() -> None:
    first_num = get_some_input()
    second_num = get_some_input()

    new_num = do_some_math(first_num, second_num)

    print(f"Your new number is {new_num}")

main()
```

Here we go. This code should ask the user for two numbers, cast them into ints, do some math, and print out a nice message.

## Some Hard Stuff

Let's turn that Python code into Java! First, let's redefine those functions we're gonna need:

```java
package mypackage;

public class MyClass {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

	public static int getSomeInput() {

	}

	public static int doSomeMath(int num1, int num2) {

	}

}
```

That's not too bad! Let's walk through this:

Our `main` was already there, and we didn't really need to change it, which is good.

We need to make sure all our functions are `static`, or our code is gonna get mad at us. Don't worry about it too much yet.

`getSomeInput` has been camelCased, as well as we've specified it's gonna return an `int`!

`doSomeMath` needs a couple parameters, but that's no big deal, we know they're gonna be `int`s!

This code is erroring like crazy right now, and it's because Java is mad that we're not returning anything in our new methods! We say we're gonna return some `int`s, but we never do! Let's fix that.

## Doing Some Math

Let's work on this `doSomeMath` method a bit. I'm just gonna paste in my Python code right into there, and see what happens...

```java
public static int doSomeMath(int num1, int num2) {
❌   new_num = 0
❌   num1 = num1 * num2
❌   new_num = num1 + 5
❌   num2 += 1
❌   num1 -= 1
❌   return new_num - num1 + num2
}
```

I've taken the liberty of adding errors on every line for you, since there are errors on every line. Hovering over one of these errors, we get:

```
Syntax error, insert ";" to complete Statement
```

You're gonna get a million of these, so get used to it. Remember when I said we need a semicolon at the end of every line that doesn't have a curly bracket? Yeah, we need those. I'll add 'em.

```java
public static int doSomeMath(int num1, int num2) {
❌   new_num = 0
     num1 = num1 * num2
❌   new_num = num1 + 5
     num2 += 1
     num1 -= 1
❌   return new_num - num1 + num2
}
```

It may not look like it, but that's waaaaay better. Take a minute here to find the commonality on all the erroring lines now... Got it? That `new_num` variable is giving us a ton of trouble: why?

Java is a **Statically Typed Langauge**, which means we need to tell the code what type of data each variable is going to represent **the moment we define the variable**. In this case, we want to tell `new_num` that it's an `int` when we define it, so let's do that!

```java
public static int doSomeMath(int num1, int num2) {
    int new_num = 0;
    num1 = num1 * num2;
    new_num = num1 + 5;
    num2 += 1;
    num1 -= 1;
    return new_num - num1 + num2;
}
```

Errorless. A thing of beauty, really. We've now told `new_num` that it's an int when we created it, and now everyone else knows what `new_num` is! Easy!

### Cleaning Our Gross Python Code

Let's clean this code up a bit, to make it more Java-like. First, we don't use snake_case anymore, so let's switch these over to camelCase.

```java
public static int doSomeMath(int num1, int num2) {
    int newNum = 0;
    num1 = num1 * num2;
    newNum = num1 + 5;
    num2 += 1;
    num1 -= 1;
    return newNum - num1 + num2;
}
```

Much better. Let's deal with a couple other things:

1. See how we're doing `variable += 1` and `variable -= 1`. This is so common in Java that there's a shortcut for it: `variable++` or `variable--`! It's called the increment or decrement operator, and it's a nice little shortcut of subtracting by 1!

2. That `num1 = num1 * num2;` line is kind of gross, so let's just... `num1 *= num2;`. That's a Python thing too, I'm just dumb.

After all that, we should get:

```java
public static int doSomeMath(int num1, int num2) {
    int newNum = 0;
    num1 *= num2;
    newNum = num1 + 5;
    num2++;
    num1--;
    return newNum - num1 + num2;
}
```

Beautiful.

## Input Time!

Python was a blessing, as the `input()` function was built right in, and was really nice and easy. Java hates you. Java no give you `input()`. Java give you `Scanner`.

```java
import java.util.Scanner;
```

Schmack that guy underneath your package at the top of your file. No built-in input reading for you! Let's go look at our `get_some_input` Python code.

```py
def get_some_input() -> int:
    number = int(input("Please give me a whole number!"))
    return number
```

Now, let's rebuild this in Java!

```java
public static int getSomeInput() {
    Scanner scanner = new Scanner(System.in);

    System.out.println("Please give me a whole number!");

    int number = scanner.nextInt();

    return number;

}
```

Just puked all over my keyboard. Maybe cause I'm sick, sure, but just look at how gross that code is! What happened to our nice two line function? This looks more like file reading than getting input! You're not too far off there. Let's break this down:

- `Scanner scanner = new Scanner(System.in);`

  - Remember creating and using objects in Python? `Scanner` is an object! We're creating a new `Scanner` object, calling it `Scanner`, and giving it the argument of `System.in`.
  - `System` is also an object, but it's a really fancy one. It has a bunch of built in methods and data we're gonna need access to, like the `in` variable, which is representative of our input!
  - Note that we need to keep telling Java what kind of data our variable is gonna be when we define it, hence the `Scanner` at the beginning of the line.

- `System.out.println("Please give me a whole number!");`

  - We need access to that pesky `System` object again, so we can get access to it's `out` variable. This `out` variable has a method built into it called `println()`, which prints a new line in the console. Remember Python `print()`? This is her big sister.

- `int number = scanner.nextInt();`

  - This is a nice little feature of Java. We've created a new variable of the type `int`, and named it `number`. We've then assigned `number` to `scanner.nextInt();`. That method is going tro return the next integer our scanner picks up from the console input we're gonna give it. We don't even need to cast it!

- `scanner.close();`

  - We don't need our scanner anymore, so let's close it.

- `return number;`
  - Guess.

### Maybe we want to cast a string to an int!

Welp, here's the updated code for that:

```java
public static int getSomeInput() {
    Scanner scanner = new Scanner(System.in);

    System.out.println("Please give me a whole number!");

    int number = Integer.parseInt(scanner.nextLine());

    scanner.close();

    return number;

}
```

We only changed one line! First, instead of doing `nextInt();`, we're getting the `nextLine();`, which returns a `String`. In order to cast that into an `int`, we need access to the `Integer` class. `Integer` is like `int`'s big brother, and has a bunch of tools inside it that we need access to. `parseInt();` takes a string, and returns an `int`! Watch out though, as there's a reason we use `nextInt();` instead of casting: this can error and crash.

## Jigsaw Falling Into Place

Radiohead reference, sorry. Anyways, let's finish off this code in out `main` method!

```java
public static void main(String[] args) {
    int firstNum = getSomeInput();
    int secondNum = getSomeInput();

    int newNum = doSomeMath(firstNum, secondNum);

    System.out.println("Your new number is " + newNum);
}
```

Nothing new here, we knew all this already. Alright, let's hit the big green arrow at the top of the window and run!

Aaaaaand...

```
Please give me a whole number!
5
Please give me a whole number!
Exception in thread "main" java.util.NoSuchElementException
	at java.base/java.util.Scanner.throwFor(Scanner.java:937)
	at java.base/java.util.Scanner.next(Scanner.java:1594)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2258)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2212)
	at mypackage.MyClass.getSomeInput(MyClass.java:21)
	at mypackage.MyClass.main(MyClass.java:9)
```

Huh. That's weird. Do we just suck at this? Nope, it's Java who sucks. Time for some quick [Googling](https://stackoverflow.com/questions/13042008/java-util-nosuchelementexception-scanner-reading-user-input) aaaand... Now we know the issue.

When we closed our scanner, we closed all future input, and therefore gave our second scanner nothing to read, so it crashed. Easy enough fix, let's just not close our scanner! Delete that line!

Note: This isn't a major issue _yet_. There are better ways to deal with this, but I don't care at the moment. This will work for our purposes.

```
Please give me a whole number!
5
Please give me a whole number!
5
Your new number is 12
```

WOOHOOOO! IT WORKS! HAHAHAHAHHA IT WORKS!!

## The moral of the story

This should hopefully run through some basic Java syntax and structure, and hopefully give you an understanding of the differences between Java and Python.

If you want some more stuff to work on, try these projects:

- Calculate the area of a triangle, after asking for the side lengths.
- Create a super simple chatbot, where it asks questions and you give answers. If you want to do decisions and if statements, try it!
- Try redoing the Haversine problem!
