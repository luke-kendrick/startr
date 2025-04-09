# Putting R to Work

In this chapter you will start using code and putting RStudio to work! We will begin with very basic code so that you become familiar with the layout and how entering code works.

## What Day is it Today?

Let's begin with something really simple.

When RStudio is open you want to make sure you have four panels, with the top left panel (script) open and ready. This is where you can type in any code.

Type the code below into your script now.


```r
date()
```

**Tip:** You can also just copy and paste the code into your script.

Once you have typed in your code, you are ready to run it. That is, you are going to instruct RStudio to tell you today's date.

To run the code you can leave your cursor at the end of the line of code and press `Control` + `Enter` on your keyboard (`Command` + `Enter` on a Mac). You might also notice on the top right of your script panel there is a button called `run`. This will also run your line of code but I'd recommend getting used to using the keyboard.

\newpage

Once you have run the line of code, take a look at the **console** (bottom left panel). If it has worked you should see today's date:


```r
date()
#> [1] "Tue Mar 25 19:48:13 2025"
```

Congratulations! You have entered the world of coding.

What else can RStudio do? It can be helpful to also think of the script panel as a very fancy calculator. With this in mind, let's try out some maths sums. Run the following code:


```r
20+80
```

If you ran it successfully you should see the answer appear in the **console** (bottom left panel)

Next, try a really complex sum:


```r
12345*54321
```

Note that we need to use `*` an asterisk to signify this is a multiplication sum. Run the line of code and check out the answer. In case you needed to know the answer to 12345 x 54321, RStudio has got you covered!

Hopefully now you are starting to see the very basics of how you should input code into RStudio and where to check to see the output.

## R Functions and Arguments: A Piece of Pi

In the previous section, you ran a **function** called `date()`. In R, a **function** is a bit of code that performs a specific task. Functions have brackets at the end of them, for example `date()` is a function which returns the current date and time.

An \*\*argument\*\* is a piece of information that you pass to a function, which will change the way the function behaves. Let's look at an example.

The code below will use the function called `round()`. Within this function (inside the parentheses) I can enter an **argument**. I've entered the mathematical constant pi here as the argument.

The function `round()` with pi `π` entered as an argument (inside the parentheses) will just round the value to the nearest whole number.


```r
round(3.14159265359)
#> [1] 3
```

However, what if I wanted this to two-decimal places? No problem! Simply add another argument. Some functions will contain multiple arguments.

Run the code below and check your console to see the output.


```r
round(3.14159265359, digits = 2)
```

Here we have use a `,` comma to separate the arguments within the parentheses. Here I have used `digits = 2` to change the behaviour of this function by rounding pi `π` to two decimal places.

As you advance further with R code you'll be using lots of different functions and arguments.

If at any point you want to learn about a function, we can use `?`. Try running the code below:


```r
?round()
```

If you ran it successfully you will notice in the **output panel** (bottom right) that the **help** tab is now showing documentation to explain how this function works, including all the possible arguments.

You can use `?` at any time to see how a function works.

## R Comments are Human Notes

You might be a little worried that eventually you are going to have to remember so much code. The base version of R contains thousands of functions, even before we start using **packages**! (more on those later). One concern people have with code is needing to remember everything.

To deal with this issue, when writing our code, we should use comments in our R script. A comment is a piece of text which you can enter in your code as a note. I like to think of comments as human notes, as RStudio does not read them.

In order to tell RStudio where our human notes begin we need to use `#` hashtag. Anything written after a hashtag is not processed or read by RStudio. Check out the example below:


```r
date() #this will ask for today's date

round(3.14159265359, digits = 2) #this rounds a value to two decimal places
```

You should use notes routinely when writing code for two important reasons:

1.  It will help remind you how your code works if you look at it again in the future.

2.  If you send or share your code with someone else your notes can help them to understand your code.

Therefore, here we have our first important rule:

> **Always make use of comments when coding in RStudio (\#)**

Before moving on to the next section, head back into RStudio and add some notes to your R script.

## Creating Objects

Another important feature is knowing how to create an **object**. Variables and/or data can be assigned to objects, however, you need to create the object. Let's look at an example. Run the code below.


```r
myobject <- c(1, 2, 3, 4)
```

Let's talk through this code step by step:

-   What you might notice is that I have created an object called `myobject` (a truly inspirational name). You can call an object anything you like.

-   Next I have used an arrow `<-`. This means that anything presented on the right hand side of this arrow will be committed to this object.

-   Then I used `c()` which allows us to list values. I want to create a mini data set with the numbers 1-4.

After running this code, nothing particularly thrilling will happen and you may notice that the console does not return anything exciting. However, take a look at the **environment** panel (top right) and what do you notice?

If it has worked, you should spot that there is an object called `myobject` (or whatever you called yours). Just like in Figure \@ref(fig:fig-environment).

<div class="figure" style="text-align: center">
<img src="images/object.png" alt="The environment contains the new object called `myobject`." width="100%" />
<p class="caption">(\#fig:fig-environment)The environment contains the new object called `myobject`.</p>
</div>

Everything that exists is an object. Everything that happens is a function.
