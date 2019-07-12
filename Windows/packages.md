# Handling Packages in cx

## Setup

To understand packages we will use three packages and call different functions from each, pointing to another package.

First of all make three packages or just download them [here](https://github.com) and put them in your workdirectory.

*For example: D:\...\CX\examples*

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/1.jpg" width="400">

to run cx with different packages we have to run the **cx** command followed by each package.

With this example this would look like this:

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/2.jpg" width="400">

if you had another package called 'package3.cx' you would just add it at the end.\
*cx main.cx package1.cx package2.cx package3.cx*

The output of our example should then look like this:

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/3.jpg" width="400">

The question now is, why?

## Understanding package handling

### main.cx
#### Imports and Declarations

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/4.jpg" width="400">

In **line 6** we declare how the package itself is named -> *main*\
In **line 18** we import the package with the name *package1*\
In **line 19** we import the package with the name *package2*\

In **line 31** we define a *string* variable called 'MAIN_VARIABLE_STRING_1' and declare its Value is 'Variable of main #1'\
In **line 32** we define a *string* variable called 'MAIN_VARIABLE_STRING_2' and declare its Value is 'Variable of main #2'\

In **line 34** we define a *Struct1* variable called 'MAIN_VARIABLE_STRUCT1' from package1\
! This Structure is not declared in the main-package but in package1.\
To use a struct from another package you have to **import** this package (which we did in **line18**)\
Also for sure it has to be defined in the other package:

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/6.jpg" width="400">

Here we see in package *package1* we have declared **Struct1** in line 24

#### Functions

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/5.jpg" width="900">

Within main.cx we have defined one function called *main*.\
There you can see different calls of functions and variables.

If you want to use a variable or a function from another package you always have to **import** it and then start with the package name,\ followed by a **.** and then the function or variable you want to use:

*packageName*.**functionName()** or *packagename*.**variableName**

### Following the code

Let's just try to understand what is happening on this example:

main.cx.42: **package1.fillStruct1()** -> we call function fillStruct1() in package1. (Thats package1.cx.41)\

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/7.jpg" width="900">

we take the value in **MAIN_VARIABLE_STRING1** and write it into **variableOfStruct1.name**\
Let's have a look what is stored in this variable. So we search for our definition and declaration in the **main** package\
main.cx.31: **MAIN_VARIABLE_STRING_1 str = "Variable of main #1"** -> so the value we store in **variableOfStruct1.name** is **"Variable of main #1**

Also we take the variable declared in package1 **variableOfId** and put it in **variableOfStruct1.id**

So our Struct1 is now full with information.

Let's jump back to our main, cause that is what happens now.

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/8.jpg" width="900">

Now we have got three diferent approaches to print out what we just have stored

#### **variant1**: 
We define a string variable and declare its value by using a function of package1 called *getStruct1Name*. You see that we    also pass a variable to the function because we declared it like that in package1. 

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/9.jpg" width="900">

You see, we have to pass a **Struct1 variable** and will get back a **String variable** that we than can store in our ***bufferstring1* variable** in main.

After that we just str.print the String variable: str.print(bufferstring)

#### **varaint2**:
Just like variant1 just we pass the output of our method straight to the str.print function.

#### **variant3**:
Here we just directly pass the name value stored in the variable **variableOfStruct1** accessed by the following **.name** to the str.print

### Excercise
<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/10.jpg" width="400">

To try to understand you also have to write code yourself so try to change these lines so that you output the **id** of the Struct2 of package2.

*hint: to print i32 variable you have to use i32.print(variable)*

### Struct with variable of another package

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/11.jpg" width="400">

Here you see that we have defined another structure in package2. Now we added another variable with the name **structure1**.\
See that it is another **Struct1** declared in **package1**.
Don't forget, to use this we also have to **import "package1"**.

So first we call **fillStruct2_1()** of package2:

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/12.jpg" width="400">

Here we first call **fillStructForPackage2()** of package1:

<img src="https://raw.githubusercontent.com/4rchim3d3s/cx-tutorials/master/Windows/cx%20packages/13.jpg" width="400">

And then declare all variables of this special struct.\
See that we save the variable **variableOfStruct1ForPackage2** of **package1** into the Struct-Variable called **variableOfStruct2_2** of *Struct2_1* out of package2.

After that you see how you can access the values and print them out.

## Bugs

By now i only got a bug with defining an Array of a Structure of another package within a Structure. 
See https://github.com/skycoin/cx/issues/385 if it got fixed.

A workaround is to just redefine the same structure within the package, see also the link above.
