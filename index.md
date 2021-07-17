---
title:Getting started with PHP Constants
---
### Introduction
In layman's terms, when something is said to be constant, it means that nothing can be done to alter it any way, even over time. 
It is not any different with constants in the PHP context. In fact, Constants here 
are names that when defined, cannot be altered. Shortly, we will dive more into its intricacies.

### What we will cover
1. What a PHP Constant is.
2. PHP Constant naming conventions
3. How to define a PHP Constant.
4. Differences between Constants and Variables.

### Prerequisites
Before getting into it, you atleat have to know the following concepts and install the following tools in your machine.
1. Possess a basic PHP language understanding.
2. Installed xampp which you could get from [here](https://www.apachefriends.org/download.html) or wampp from [here](https://sourceforge.net/projects/wampserver/). These softwares run the PHP scripts.
3. Have installed a text editor you prefer. I will be using VS Code to run basic code from this article which you could install from [here](https://visualstudio.microsoft.com/downloads/).

Ready to learn? Let's begin!

### What a PHP Constant is
From the above covered introduction, constants can be compared to but not the same as variables. 
Unlike variables, once we initialize or define a constant, we cannot alter the 
value attached to it when executing a script at any point in time. 
Of course there exists an exception for this condition when we use (magic constants) instead. We will not cover magic constants in this article but you could 
find content on the same from [here](https://www.tutorialrepublic.com/php-tutorial/php-magic-constants.php) that explain magic constants profoundly.
Due to their immutable nature, PHP Constants come in handy when defining data like configuration settings including website's base URL, database unername and passwords, to mention but a few. 

### PHP Constants naming conventions
It is important to note that PHP Constants are case sentive before we proceed.
Names of constants **must** begin with either a letter or an underscore(_). 
Next when we see how to create a constant, we will also see that the constant names are **always** in uppercase.

### Defining the PHP Constant
Now that we have a glimpse of what the constant is, let's see how we could create one.
The define() function is what we use when creating the constant. It has three parameters passed to it and these are:
 1. Name: This references the what you call your defined constant.
 2. Value: value that is attached to the defined constant name.
 3. case_insensitive: Which is optional as an argument passed and implies a constant being case-insensitive. The default value for this is **false** 
    implying the constant being case-sensitive and **true** if case-insensitive.

Below is the syntax used:
```bash
define(name, value, case_insensitive)
```

```php
<?php
  //Defining a a case-sensitive onstant
  define("NAME", "Neema Muganga");
  echo NAME, "\n";

  //Define a case-insensitve constant
  define("NAME", "Neema Muganga", true);
  
  //because we passed true for case-insensitive parameter, we could echo the constant in lowercase
  echo name;
?>
```

The above code will output:

```bash
Neema Muganga
```

In this context, I would love to introduce the **constant()** function that is used to retrieve the value of the constant by passing in the ***name*** of the constant as a parameter.
Therefore in a different example code:

 ```php
<?php
  //Defining  Constant
  define("CITY", "Mombasa");

  echo CITY, "\n";
  
  //this will ouput same value as echo statement above
  echo constant("CITY");
?>
```
Output will be:

```bash
Mombasa
Mombasa
```

Now you have an understanding of constants, how to define the and how to retrieve their values.
Next, we will cover the **magic constants** we briefly mentioned when we were defining a constant above. 

### Magic Constants
These type of constants are different from the normal constants in that when defined, they can change
their value even when the scripts is executing. We will only cover a few and how they can be implemented.


Constants referenced to variables that cannot be changes after being defined.
unlike normal variables in PHP that start with the '$' sign during initialization, constants should start with 
an underscore or a letter.