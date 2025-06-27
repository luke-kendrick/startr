# Putting R to Work

In this chapter you will start using code and putting RStudio to work! We will begin with very basic code so that you become familiar with the layout and how entering code works.

## What Day is it Today?

Let's begin with something really simple.

When RStudio is open you want to make sure you have four panels, with the top left panel (script) open and ready. This is where you can type your code.

Type the code below into your script now.


```r
date()
```

Once you have typed in your code, you are ready to run it. This means you will ask RStudio to tell you today's date.

To run the code you can leave your cursor at the end of the line of code and use your keyboard to press `Control` + `Enter` or `Command` + `Enter` on a Mac. You might also notice on the top right of your script panel there is a button called `run`. This will also run the line of code but I'd recommend getting used to using the keyboard.

\newpage

Once you have run the line of code, take a look at the **console** (bottom left panel). If it has worked you should see today's date:


```r
date()
#> [1] "Fri Jun 27 13:15:12 2025"
```

Congratulations! You have entered the world of coding.

Well, what else can RStudio do? It can be helpful to also think of the script panel as a very fancy calculator. With this in mind, let's try out some maths sums. Run the following code:


```r
20+80
```

If you ran it successfully you should see the answer appear in the **console** (bottom left panel).

Next, try a really complex sum:


```r
12345*54321
```

Note that we need to use `*` an asterisk to signify this is a multiplication sum. Run the line of code and check out the answer. In case you needed to know the answer to 12345 x 54321, RStudio is there for you!

Hopefully now you are starting to see the very basics of how you should input code into RStudio and where to check to see the output.

## Functions and Arguments: A Piece of Pi

In the previous section, you ran a bit of code which is a **function** called `date()`. In R, a **function** is a bit of code that performs a specific task. Functions have parentheses `()` at the end, for example `date()` is a function which returns the current date and time.

An **argument** is a piece of information that you pass into a function, which will change the way the function behaves. Let's look at an example.

The code below will use the function called `round()`. Within this function (inside the parentheses) I can enter an **argument**. I've entered the mathematical constant pi here as the argument.

The function `round()` with pi `π` entered as an argument (inside the parentheses) will just round the value to the nearest whole number. Try this yourself in RStudio now.


```r
round(3.14159265359)
#> [1] 3
round(pi) # or you can just type `pi`
#> [1] 3
```

However, what if I wanted this output to two-decimal places? No problem! Simply add another argument. Some functions will contain multiple arguments, but for now let's keep it simple.

Run the code below and check your console to see the output.


```r
round(3.14159265359, digits = 2)
```

Here we have use a `,` comma to separate the arguments within the parentheses. The argument `digits = 2` can be used to change the behaviour of this function by rounding pi `π` to two decimal places. An **argument** will give a function some more specific guidance.

As you advance further with R code you'll be using lots of different functions and arguments.

If at any point you want to learn about a function, we can use `?`. Try running the code below:


```r
?round()
```

If you ran it successfully you will notice in the **output panel** (bottom right) that the **help** tab is now showing documentation to explain how this function works, including all the possible arguments.

You can use `?` at any time to see how a function works.

## Comments = Human Notes

You might be a little worried that eventually you are going to have to remember so much code. The base version of R contains thousands of functions, even before we start using **packages**! (more on packages later). One concern people have with code is needing to remember everything.

To deal with this issue, when writing our code, we should use comments in our R script. A **comment** is a piece of text which you can add next to your code as a note. I like to think of comments as "human notes", we can read them but RStudio will ignore them.

In order to tell RStudio where our human notes begin we need to use `#` hashtag. Anything written after the hashtag is not processed or read by RStudio. Check out the example below:


```r
date() #this will ask for today's date

round(3.14159265359, digits = 2) #this rounds a value to two decimal places
```

Rstudio will run those **functions** but the notes are there for your benefit. You should use notes routinely when writing code for two important reasons:

1.  It will help remind you how your code works if you look at it again in the future.

2.  If you send or share your code with someone else, your notes can help them to understand what you've done and why.

Therefore, here we have our first important rule:

> **Always make use of comments when coding in RStudio (\#)**

Before moving on to the next section, head back into RStudio and practice adding some notes to your R script. Remember to use the `#` hashtag. Once you've finished writing your notes, hit enter and then the script moves to the next line ready for the next bit of code.

## Creating Objects

Another important feature is knowing how to create an **object**. Variables and/or data can be assigned to objects, however, you need to create the object yourself. Let's look at an example. Run the code below:


```r
myobject <- c(1, 2, 3, 4)
```

Let's talk through this code step by step:

-   What you might notice is that I have created an object called `myobject` (a truly inspirational name). This is on the very left of this line of code. You can call an object anything you like, so feel free to call it something else.

-   Next I have used an arrow `<-`. This means that anything written on the right hand side of this arrow will be committed to this object. This arrow is called an assignment operator.

-   Then I used `c()` which is a function that allows us to list values. I created a mini data set with the numbers 1-4.

Go ahead if you haven't already and run that bit of code, nothing particularly thrilling will happen and you may notice that the console does not return anything exciting. However, take a look at the **environment** panel (top right) and what do you notice?

If it has worked, you should spot that there is an object called `myobject` (or whatever you called yours) as shown in Figure \@ref(fig:fig-environment).

<div class="figure" style="text-align: center">
<img src="images/object.png" alt="The environment contains the new object called `myobject`." width="100%" />
<p class="caption">(\#fig:fig-environment)The environment contains the new object called `myobject`.</p>
</div>

> In the R world:
>
> -   Everything that exists is an object.
>
> -   Everything that happens is a function.

Almost anything can be committed to an object in RStudio. For example, run and adapt the code below. Change "Luke" to your own name! Then check that your environment looks like Figure \@ref(fig:fig-environment-1).


```r
name <- "Luke"
answer <- 12345*54321
pi <- round(3.14159265359, digits = 2)
```

<div class="figure" style="text-align: center">
<img src="images/environment.png" alt="The environment contains multiple new objects." width="100%" />
<p class="caption">(\#fig:fig-environment-1)The environment contains multiple new objects.</p>
</div>

We can also print an object to the console. Essentially this will ask RStudio to just show the contents of an object in the console. You should try this with the `print()` function, see below.


```r
print(myobject)
print(name)
print(answer)
print(pi)
```

### **Naming and Removing Objects**

I did say that you can call an object anything you like. One thing that will help is to try and keep object names short. That is because often you might need to keep typing out object names, particularly if you use the object frequently (e.g., an object that contains your data set for analysis).

Generally, avoid using multiple words and keep it short and informative.


```r
what_is_my_first_name <- "Luke" # this is not a good object name. it is too long.
name <- "Luke" # this is a short informative object name
```

Finally, if you want to remove an object from your environment you can use the code below:


```r
rm(myobject, name, answer, pi) # will remove these four objects.

rm(list = ls()) # will remove EVERYTHING from the environment.
```

## Troubleshooting and Getting Help with R

During the early stages of learning to code it is not uncommon to come across error messages. Sometimes the code will not work and this can be frustrating. Also, some error messages are a little tricky to interpret. Thankfully there are options for support to troubleshoot issues.

Firstly, remember to use `?` in front of a function to check out the documentation to ensure you are using it correctly. If I wanted to learn about the `rm()` function from the previous section I would use:


```r
?rm()
```

Secondly, if you come across an error message and you cannot figure it out/it looks a load of gibberish, copy and paste the error message into Google. It is likely that someone else would have experienced this error and there is probably a solution already online.

Finally, one of the most common issues when learning to code is the presence of a typo. When you code in RStudio it needs to be written very specifically and how it expects it to be written. RStudio will not work if you make a typo. Similarly, R code is case sensitive. `myobject` is not the same as `MYOBJECT` or `mYobject`.

Take your time to check you code carefully when you are starting out in R, most errors tend to be small typos.

Therefore, here we have our second important rule:

> **Check your code for typos and enter it exactly as R expects**

## Chapter Summary

You should now have an understanding of how functions and arguments work. You should also have ran your very first lines of code! Congratulations, you are officially an R coder. You should also now be able to create objects, name them appropriately, and remove them from the environment. Finally, you should be aware of two key rules: (1) use comments to make notes with you code and (2) enter code exactly intended and check out for typos. In the next chapter you will begin to work with packages and learn how to import a data set into RStudio ready for data analysis.
