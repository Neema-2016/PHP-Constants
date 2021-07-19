---
title: Getting started with PHP Constants
---
### Introduction
In layman's terms, when something is said to be constant, it means that nothing it can not be altered any way, even over time. 
It is not any different with constants in the PHP context. In fact, constants here are names or identifiers that when defined, cannot be altered. Shortly, we will dive more into its intricacies.

### What we will cover
1. What a PHP Constant is.
2. PHP Constant naming conventions
3. How to define a PHP Constant.
4. Differences between Constants and Variables.

### Prerequisites
Before getting into it, you at least have to know the following concepts and install the following tools in your machine.
1. Possess a basic PHP language understanding.
2. Installed xampp which you could get from [here](https://www.apachefriends.org/download.html) or wampp from [here](https://sourceforge.net/projects/wampserver/). These softwares run the PHP scripts.
3. Have installed a text editor you prefer. I will be using VS Code to run basic code from this article which you could install from [this](https://visualstudio.microsoft.com/downloads/) link.

Ready to learn? Let's begin!

### What a PHP Constant is
From the above covered introduction, constants can be compared to but not the same as variables. 
Unlike variables, once we initialize or define a constant, we cannot change the value attached to it when executing a script at any point in time. 
Of course there exists an exception for this condition when we use (magic constants) instead. We will not cover magic constants in this article but you could 
find content on the same from [here](https://www.tutorialrepublic.com/php-tutorial/php-magic-constants.php) that explains magic constants concept profoundly.
Due to their immutable nature, PHP Constants come in handy when defining data like configuration settings including website's base URL, database username and passwords, to mention but a few. 

### PHP Constants naming conventions
It is important to note that PHP Constants are **case sensitive** .
Also, when naming constants, they **must** begin with either a letter or an *underscore(_)*. 
Next when we get to create a constant, we will also see that the constant names are **always** in uppercase.

### Defining the PHP Constant
Now that we have some basic understanding of what a constant is, let's see how we could create one.
The define() function is what we use when creating it. Three parameters are passed to it and these are:
 1. Name: This references to what you call your defined constant.
 2. Value: The value that is attached to the constant name.
 3. case insensitive: Which is optional as a passed parameter and implies that a constant is case-insensitive. This parameter has two values: *True* and *False*. The default value for this parameter is **false** implying the constant being case-sensitive and **true** if case-insensitive.
> Remember constant names are always written in uppercase when defining and accessing their values. Therefore, when this parameter is set to *true*, you could write it in lowercase when accessing its value. Soon we will see this statement making better sense. 

Below is the syntax used:
```bash
define(name, value, case_insensitive)
```

```php
<?php
  //Defining a a case-sensitive constant
  define("NAME", "Neema Muganga");
  echo NAME, "\n"; //Notice here, we write the constant name in uppercase as is required. By default, it is case-sensitive.

  //Defining a case-insensitve constant
  define("NAME", "Neema Muganga", true);
  
  //because we passed true for case-insensitive parameter, we could echo the value of the constant with the name written in lowercase.
  echo name;
?>
```

The above code will output:

```bash
Neema Muganga
Neema Muganga
```

In this context, I will introduce the **constant()** function that is used to retrieve the value of the constant by passing in the ***name*** of the constant as a parameter. This function is especially useful when we need to access a constant value whose name is not known.

Therefore in a different example code, the syntax will be as below:

 ```php
<?php
  //Defining the Constant
  define("CITY", "Mombasa");

  echo CITY, "\n";
  
  //this will output same value as echo statement above
  echo constant("CITY");
?>
```
Output will be:

```bash
Mombasa
Mombasa
```

So far so good. Now we know what a constant is, why and when it could be used, how to create one and how to finally access its value. 
Should the concept still feel unclear, please go through the article a second time and everything will make perfect sense.

Lastly, we will see how different constants are from variables just to clear any possible uncertainties when it comes to these two concepts.

### Differences between Constants and Variables
1. First, we have already seen that unlike variables that start with the **'$'** sign, constants begin with either an underscore **'_'** or a letter.
2. We also mentioned that constant values remain unchanged once defined unlike variables whose value can be changed to a something different.
3. Defining a constant is only done using the define() function, while we could define variables using assignment statements of values attached to the variable names that begin with a '$' sign.
4. In terms of scope, constants maintain a global scope. That is, they can be accessed from anywhere within a script. Variables on the other hand have their scope depending on where they have been defined in the script. Either globally or locally. You could read more about scope in PHP from [this](https://www.w3schools.com/php/php_variables_scope.asp) link to understand this distinction better.

That was fun! Now I hope you got the PHP constants concept well. 
Remember, you learn best by doing.

Happy Coding!