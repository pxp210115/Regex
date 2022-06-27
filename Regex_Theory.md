# Regex - 
## Understanding Regex and text manipulation techniques

A '?' will match a single character with any value.

An '*' will match any number of chracter with any value.

A Regular expression is a mixture of literals (the exact chracters) and meta chracters (*/?).

![image](https://user-images.githubusercontent.com/100412162/176047589-b7fdca0c-359c-47c7-b170-aa4f0cd38a8a.png)

The above image will find one match, as there is one word that matches the regex expression.

**Note** 📝 :- If we wanted to use metacharacters and search exactly for them, then we use the '\' or the escape character.

In regular expressions, there are twelve metacharacters that should be escaped if they are to be used with their literal meaning:

• Backslash \

• Caret ^

• Dollar sign $

• Dot.

• Pipe symbol |

• Question mark ?

• Asterisk *

• Plus sign +

• Opening parenthesis (

• Closing parenthesis )

• Opening square bracket [

• The opening curly brace {

## Character classes:-

Character classes allows us to define a set of literals that can be matched with the string. It is denoted by [].

![image](https://user-images.githubusercontent.com/100412162/176048487-4c53f3c0-d61f-4d0c-8e89-c5f3a4c7f346.png)

The above regex expression gives us a match if the literal at the index is either a [c/s].

We can use ranges to define a specific type of literal and then get a match

**[0-9]** - Any numeric 

**[a-z]** - Any small case alphanumeral

**[A-Z]** - Any large case alphanumeral

**Note** 📝:- We can use all of them together to get something like a literal that matches any of the three criteria by [0-9a-zA-Z].

We can also declare the negation of the set for matching purposes by using the '^' symbol.

**[^0-9]** - Means there shall be a match if that character does not match the required criteria thus mentioned.

## Some special regex matching functions that have already been shortcuted:-

![image](https://user-images.githubusercontent.com/100412162/176049677-60038d85-829f-4852-9a05-9584fc9ba7c3.png)

The dot '.' character is the most widely used where the '.' can represent anything but a newline character (\n).

To add multiple values into the regex function we use:-

**Eg:**- '/License: (yes/no)/' - This allows us to alternate between License: yes and License: no.

## Quanitifiers

Quantifiers are always applied to the previous token.

![image](https://user-images.githubusercontent.com/100412162/176051577-306dc4ee-ada8-49e6-b98f-1b466cf08ef1.png)

**Eg:**- '/cars?/' - Tells us to match the letters c,a,r and s but the '?' tells us that the character 's' is optional.

## Greedy and Reluctant quantifiers:-

**Eg:**- '/".+"/' for  English "Hello", Spanish "Hola"
This indicates that we can have any character '.', '+' number of times i.e 1 or more number of times. We can expect that it specifically picks up "Hello" and "Hola" but however due to the greedy nature of the quantiifer we shall get the chracters between the most extreme quotes.

**Note **📝:- Greedy nature comes by default to the regex expressions. We can make any quantiifer non-greedy by using the '?' at the end of the regex expression.

![image](https://user-images.githubusercontent.com/100412162/176052469-028939af-d1a5-4729-8fdf-fccdb643832a.png)

## Boundary characters:-

'^' - Indicates the start of a sentence for a match

'$' - Indicates the end of a sentence for a match

**Eg:**-  '/^Name:[\sa-zA-Z]+$/' - Indicates that the sentence shall start with 'Name:' and it will be followed by a space('\s') and an alphanumeral that can be the small case/big case. The '+' sign afterwards indicates that the whole match in brackets can be repeated 1 or more times and the '$' sign indicates that, it is the end of the sentence.

