---
layout: tutorials
author: MRBDR
tags: [programmation, microstudio]
permalink: /tutoriels/fonctions-variables
---

<h3>Créer du code avec MicroStudio et Python</h3>

![L'interface de MicroStudio](/images/MicroStudio-Interface.jpg)

Lorsque vous créer un nouveau projet, MicroStudio vous affichera trois fenêtre dans l'onglet **code** de votre projet.

La fenêtre de gauche est votre **éditeur de texte**, où vous allez entrer votre code. La fenêtre **Run** à droite, vous permet de lancer l'application et tester votre jeux. La fenêtre **Console** vous permet de regarder l'état de votre programme. En fait, la **Console** est comme un ordinateur qui peut lire et afficher du code.

Dans l'**édituer de texte**, effacer tout le text déjà présent et insérer le code suivant:
```
print("Bonjours à tous!")
```

Ce programme est asser fameux et quasiment tout programmeur on écrit un programme similaire lors de leur début en programmation.
Dans la **Console**, vous pouvez exécuter des commandes. Pour lancer le programme, écrivez `run` dans la **Console** et vous allez voir le résultat de votre programme à même la **Console**.

Il se peut que vous voyez du texte du genre `microscript 2.0 - beta` dans votre **Console**. Si c'est le cas, vous devez changer votre langage de programmation dans l'onglet **paramètre** de votre projet. Cet onglet se trouve à gauche. Une fois dans les **paramètres**, allez à la fin des options et cliquer sur **Montrer les options avancées** pour changer le langage de programmation à Python.

Les odrinateurs ne comprennent que des **0** et des **1**. Ainsi, lorsque vous lancez votre programme dans la **Console** Python va interpréter votre texte et le traduire dans le langage des ordinateurs.

Félicitation! Vous venez de créer votre premier programme.

<h3>Les functions</h3>

Une fonction est comme une verbe ou une action que l'ordinateur ou le langage de programmation sait déjà faire.
Dans ton programme, la fonction `print()` sait comment imprimer dans la **Console**.
La fonction print prend des arguments. Dans ce cas, `"Bonjour à tous"` est l'argument que la fonction `print()` prend.

<h3>Les Bugs</h3>

Les bugs sont des erreurs, ou, plus positivement, des problèmes à résoudre! Apprendre à corriger les bugs, fait partie du processus d'apprentissage de tout bon programmeur.
Imagine qu'on ait écrit par accient `print("hello, world"` en oubliant d'ajouter `)` pour terminer la commande. Si on fait cette erreur, lorsqu'on lance le programme, l'interprétateur de Python nous affichera un message d'erreur dans la **Console**.
Généralment, les messages d'erreur vous informent de votre erreur et des solutions possibles pour la corriger. Malheureusement, ce n'est pas toujours le cas et ce sera à vous de figurer la solution pour corriger le bug.

<h3>Améliorer votre premier programme en Python</h3>

On peut personaliser votre premier programme en Python.

Dans l'editeur de texte, on peut ajouter une autre fonction. La fonction `input()` prend un invite de commande comme arguement. On peut ainsi éditer notre code pour dire

```
input("Quel est votre nom? ")
print("Bonjour à tous!")
```

Ce seul ajout ne sera pas suffisant pour permettre à notre programme d'afficher ce que l'usager va entrer dans sa console. Pour être en mesure de faire cela, nous allons avoir besoin de ***variables**.

<h3>Les variables</h3>

Une variable est un conteneur pour une valeur dans votre programme.

Dans votre programme, vous pouvez créer une variable ainsi:

```
nom = input("Quel est votre nom? ")
print("Bonjour à tous!")
```

Remarquer le symbole **=** entre `nom` et `ìnput` qui a un rôle particulier en programmation. Ce symbole d'égalité assigne ce qui est à droite du symbole à ce qui est à gauche. Ainsi, la valeur que l'usager du programme entre avec la fonction `input("Quel est votre nom?")` sera assigné à la variable `nom`.

Éditer votre code comme suit:

```
nom = input("Quel est votre nom? ")
print("Bonjour à tous!")
```

Lorsque vous lancez votre programme, vous allez remarquer qu'il y a une erreur. En effet, le programme affiche seulement `Bonjour à tous!` dans la **Console** peut importe ce qui est écrit à l'invite de commande.

Il est donc nécessaire de modifier à nouveau notre code.

```
nom = input("Quel est votre nom? ")
print("Bonjour")
print(nom)
```

Le résultat affiché dans la **Console** de ce programme pourrait ressemblé à 

```
Quel est votre nom? David
Bonjour
David
```

Nous nous approchons du résultat attendu!
Tu peux apprendre d'avantage sur les types de données de Python dans la documentation du langage.

<h3>Les commentaires</h3>

Les commentaires sont une façon de noter dans le code ce qui est fait par le programme. Ce sont des traces pour le programmeur qui lui permet de se souvenir ce que signifie le code ou comprendre le code d'un autre programmeur. Bref, ce sont des notes pour vous ou pour vos collègues qui vont voir votre code.

Tu peux ajouter des commentaires à ton programme ainsi:

```
# Demander à l'usager son nom
nom = input("Quel est votre nom? ")
print("Bonjour")
print(nom)
```

Les commentaires peuvent aussi servir pour noter ce qui reste à faire dans votre code.

<h3>Améliorer votre premier programme en Python</h3>

On peut modifier notre code ainsi:

```
# Demander à l'usager pour leur nom
nom = input("Quel est votre nom? ")

# Afficher bonjour et le nom de l'usager
print("Bonjour " + nom)
```

Certaines fonctions accepte plusieurs arguments.

On peut utiliser la virguel `,` pour envoyer plusieurs arguments à une même fonction.

```
# Demander à l'usager pour leur nom
nom = input("Quel est votre nom? ")

# Afficer bonjour et le nom de l'usager
print("Bonjour", nom)
```

Avec ce code, la **Console** affichera `Bonjour David` si on entre `David` à l'invite de commande.

<h3>Les chaînes de charactères et les paramètres</h3>

    A string, known as a str in Python, is a sequence of text.

    Rewinding a bit in our code back to the following, there was a visual side effect of having the result appear on multiple lines:

    # Ask the user for their name
    name = input("What's your name? ")
    print("hello,")
    print(name)

    Functions take arguments that influence their behavior. If we look at the documentation for print you’ll notice we can learn a lot about the arguments that the print function takes.
    Looking at this documentation, you’ll learn that the print function automatically include a piece of code end='\n'. This \n indicates that the print function will automatically create a line break when run. The print function takes an argument called end` and the default is to create a new line.
    However, we can technically provide an argument for end ourselves such that a new line is not created!

    We can modify our code as follows:

    # Ask the user for their name
    name = input("What's your name? ")
    print("hello,", end="")
    print(name)

    By providing end="" we are over-writing the default value of end such that it never creates a new line after this first print statement. Providing the name as “David”, the output in the terminal window will be hello, David.

    Parameters, therefore, are arguments that can be taken by a function.
    You can learn more in Python’s documentation on print.

A small problem with quotation marks

    Notice how adding quotation marks as part of your string is challenging.
    print("hello,"friend"") will not work and the compiler will throw an error.
    Generally, there are two approaches to fixing this. First, you could simply change the quotes to single quote marks.
    Another, more commonly used approach would be code as print("hello, \"friend\""). The backslashes tell the compiler that the following character should be considered a quotation mark in the string and avoid a compiler error.

Formatting Strings

    Probably the most elegant way to use strings would be as follows:

    # Ask the user for their name
    name = input("What's your name? ")
    print(f"hello, {name}")

    Notice the f in print(f"hello, {name}"). This f is a special indicator to Python to treat this string a special way, different than previous approaches we have illustrated in this lecture. Expect that you will be using this style of strings quite frequently in this course.

More on Strings

    You should never expect your user will cooperate as intended. Therefore, you will need to ensure that the input of your user is corrected or checked.
    It turns out that built into strings is the ability to remove whitespace from a string.

    By utilizing the method strip on name as name = name.strip(), it will strip all the whitespaces on the left and right of the users input. You can modify your code to be:

    # Ask the user for their name
    name = input("What's your name? ")

    # Remove whitespace from the str
    name = name.strip()

    # Print the output
    print(f"hello, {name}")

    Rerunning this program, regardless of how many spaces you type before or after the name, it will strip off all the whitespace.

    Using the title method, it would title case the user’s name:

    # Ask the user for their name
    name = input("What's your name? ")

    # Remove whitespace from the str
    name = name.strip()

    # Capitalize the first letter of each word
    name = name.title()

    # Print the output
    print(f"hello, {name}")

    By this point, you might be very tired of typing python repeatedly in the terminal window. You cause us the up arrow of your keyboard to recall the most recent terminal commands you have made.

    Notice that you can modify your code to be more efficient:

    # Ask the user for their name
    name = input("What's your name? ")

    # Remove whitespace from the str and capitalize the first letter of each word
    name = name.strip().title()

    # Print the output
    print(f"hello, {name}")

    This creates the same result as your previous code.

    We could even go further!

    # Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
    name = input("What's your name? ").strip().title()

    # Print the output
    print(f"hello, {name}")

    You can learn more about strings in Python’s documentation on str

Integers or int

    In Python, an integer is referred to as an int.
    In the world of mathematics, we are familiar with +, -, *, /, and % operators. That last operator % or modulo operator may not be very familiar to you.
    You don’t have to use the text editor window in your compiler to run Python code. Down in your terminal, you can run python alone. You will be presented with >>> in the terminal window. You can then run live, interactive code. You could type 1+1 and it will run that calculation. This mode will not commonly be used during this course.
    Opening up VS Code again, we can type code calculator.py in the terminal. This will create a new file in which we will create our own calculator.

    First, we can declare a few variables.

    x = 1
    y = 2

    z = x + y

    print(z)

    Naturally, when we run python calculator.py we get the result in the terminal window of 3. We can make this more interactive using the input function.

    x = input("What's x? ")
    y = input("What's y? ")

    z = x + y

    print(z)

    Running this program, we discover that the output is incorrect as 12. Why might this be?

    Prior, we have seen how the + sign concatenates two strings. Because your input from your keyboard on your computer comes into the compiler as text, it is treated a string. We, therefore, need to convert this input from a string to an integer. We can do so as follows:

    x = input("What's x? ")
    y = input("What's y? ")

    z = int(x) + int(y)

    print(z)

    The result is now correct. The use of int(x), is called “casting” where a value is temporarily changed from one type of variable (in this case a string) to another (here, an integer).

    We can further improve our program as follows:

    x = int(input("What's x? "))
    y = int(input("What's y? "))

    print(x + y)

    This illustrates that you can run functions on functions. The most inner function is run first, and then the outer one is run. First, the input function is run. Then, the int function.
    You can learn more in Python’s Documenation of int.

Readability Wins

    When deciding on your approach to a coding task, remember that one could make a reasonable argument for many approaches to the same problem.
    Regardless of what approach you take to a programming task, remember that your code must be readable. You should use comments to give yourself and others clues about what your code is doing. Further, you should create code in a way that is readable.

Float Basics

    A floating point value is a real number that has a decimal point in it, such as 0.52.

    You can change your code to support floats as follows:

    x = float(input("What's x? "))
    y = float(input("What's y? "))

    print(x + y)

    This change allows your user to enter 1.2 and 3.4 to present a total of 4.6.

    Let’s imagine, however, that you want to round the total to the nearest integer. Looking at the Python documentation for round you’ll see that the available arguments are round(number[n, ndigits]). Those square brackets indicate that something optional can be specified by the programmer. Therefore, you could do round(n) to round a digit to its nearest integer. Alternatively, you could code as follows:

    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))

    # Create a rounded result
    z = round(x + y)

    # Print the result
    print(z)

    The output will be rounded to the nearest integer.

    What if we wanted to format the output of long numbers? For example, rather than seeing 1000, you may wish to see 1,000. You could modify your code as follows:

    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))

    # Create a rounded result
    z = round(x + y)

    # Print the formatted result
    print(f"{z:,}")

    Though quite cryptic, that print(f"{z:,}") creates a scenario where the outputted z will include commas where the result could look like 1,000 or 2,500.

More on Floats

    How can we round floating point values? First, modify your code as follows:

    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))

    # Calculate the result
    z = x / y

    # Print the result
    print(z)

    When inputting 2 as x and 3 as y, the result z is 0.6666666666 seemingly going on to infinite as we might expect.

    Let’s imagine that we want to round this down, we could modify our code as follows:

    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))

    # Calculate the result and round
    z = round(x / y, 2)

    # Print the result
    print(z)

    As we might expect, this will round the result to the nearest two decimal points.

    We could also use fstring to format the output as follows:

    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))

    # Calculate the result
    z = x / y

    # Print the result
    print(f"{z:.2f}")

    This cryptic fstring code displays the same as our prior rounding strategy.

    You can learn more in Python’s documentation of float.

Def

    Wouldn’t it be nice to create our own functions?

    Let’s bring back our final code of hello.py by typing code hello.py into the terminal window. Your starting code should look as follows:

    # Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
    name = input("What's your name? ").strip().title()

    # Print the output
    print(f"hello, {name}")

    We can better our code to create our own special function that says “hello” for us!

    Erasing all our code in our text editor, let’s start from scratch:

    name = input("What's your name? ")
    hello()
    print(name)

    Attempting to run this code, your compiler will throw an error. After all, there is no defined function for hello.

    We can create our own function called hello as follows:

    def hello():
        print("hello")


    name = input("What's your name? ")
    hello()
    print(name)

    Notice that everything under def hello() is indented. Python is an indented language. It uses indentation to understand what is part of the above function. Therefore, everything in the hello function must be indented. When something is not indented, it treats it as if it is not inside the hello function. Running python hello.py in the terminal window, you’ll see that your output is not exactly as you may want.

    We can further improve our code:


    # Create our own function
    def hello(to):
        print("hello,", to)


    # Output using our own function
    name = input("What's your name? ")
    hello(name)

    Here, in the first lines, you are creating your hello function. This time, however, you are telling the compiler that this function takes a single parameter: a variable called to. Therefore, when you call hello(name) the computer passes name into the hello function as to. This is how we pass values into functions. Very useful! Running python hello.py in the terminal window, you’ll see that the output is much closer to our ideal presented earlier in this lecture.

    We can change our code to add a default value to hello:

    # Create our own function
    def hello(to="world"):
        print("hello,", to)


    # Output using our own function
    name = input("What's your name? ")
    hello(name)

    # Output without passing the expected arguments
    hello()

    Test out your code yourself. Notice how the first hello will behave as you might expect and the second hello, which is not passed a value, will by default output hello, world.

    We don’t have to have our function at the start of our program. We can move it down, but we need to tell the compiler that we have a main function and we have a separate hello function.

    def main():

        # Output using our own function
        name = input("What's your name? ")
        hello(name)

        # Output without passing the expected arguments
        hello()


    # Create our own function
    def hello(to="world"):
        print("hello,", to)

    This alone, however, will create an error of sorts. If we run python hello.py nothing happens! The reason for this is that nothing in this code is actually calling the main function and bringing our program to life.

    The following very small modification will call the main function and restore our program to working order:

    def main():

        # Output using our own function
        name = input("What's your name? ")
        hello(name)

        # Output without passing the expected arguments
        hello()


    # Create our own function
    def hello(to="world"):
        print("hello,", to)


    main()

Returning Values

    You can imagine many scenarios where you don’t just want a function to perform an action, but also to return a value back to the main function. For example, rather than simply printing the calculation of x + y, you may want a function to return the value of this calculation back to another part of your program. This “passing back” of a value we call a return value.

    Returning to our calculator.py code by typing code calculator.py. Erase all code there. Rework the code as follows:

    def main():
        x = int(input("What's x? "))
        print("x squared is", square(x))


    def square(n):
        return n * n


    main()

    Effectively, x is passed to square. Then, the calculation of x * x is returned back to the main function.



Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit. Pellentesque vel lacinia neque. Praesent nulla quam, ullamcorper in sollicitudin ac, molestie sed justo. Cras aliquam, sapien id consectetur accumsan, augue magna faucibus ex, ut ultricies turpis tortor vel ante. In at rutrum tellus.

# Sample heading 1
## Sample heading 2
### Sample heading 3
#### Sample heading 4
##### Sample heading 5
###### Sample heading 6

Mauris viverra dictum ultricies. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod.

## Lists

Unordered:

- Fusce non velit cursus ligula mattis convallis vel at metus[^2].
- Sed pharetra tellus massa, non elementum eros vulputate non.
- Suspendisse potenti.

Ordered:

1. Quisque arcu felis, laoreet vel accumsan sit amet, fermentum at nunc.
2. Sed massa quam, auctor in eros quis, porttitor tincidunt orci.
3. Nulla convallis id sapien ornare viverra.
4. Nam a est eget ligula pellentesque posuere.

## Blockquote

The following is a blockquote:

> Suspendisse tempus dolor nec risus sodales posuere. Proin dui dui, mollis a consectetur molestie, lobortis vitae tellus.

## Thematic breaks (<hr>)

Mauris viverra dictum ultricies[^3]. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod. **You can put some text inside the horizontal rule like so.**

---
{: data-content="hr with text"}

Mauris viverra dictum ultricies. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod. **Or you can just have an clean horizontal rule.**

---

Mauris viverra dictum ultricies. Vestibulum quis ipsum euismod, facilisis metus sed, varius ipsum. Donec scelerisque lacus libero, eu dignissim sem venenatis at. Etiam id nisl ut lorem gravida euismod. Or you can just have an clean horizontal rule.

## Code

Now some code:

```
const ultimateTruth = 'follow middlepath';
console.log(ultimateTruth);
```

And here is some `inline code`!

## Tables

Now a table:

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

## Images

![theme logo](http://www.abhinavsaxena.com/images/abhinav.jpeg)

This is an image[^4]

---
{: data-content="footnotes"}

[^1]: this is a footnote. You should reach here if you click on the corresponding superscript number.
[^2]: hey there, don't forget to read all the footnotes!
[^3]: this is another footnote.
[^4]: this is a very very long footnote to test if a very very long footnote brings some problems or not; hope that there are no problems but you know sometimes problems arise from nowhere.
