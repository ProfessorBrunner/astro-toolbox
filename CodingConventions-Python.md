#Coding Conventions for Python


Let us follow some basic conventions so that our code is easily understood by others. Most of these coventions follow the  [PEP 8 -- Style Guide for Python Code](http://legacy.python.org/dev/peps/pep-0008/)

##1. Code Layout:

###(i) Indentation: 

1. Use 4 spaces per indentation level.

2. Spaces are the preferred indentation method.

3. Python 3 disallows mixing the use of tabs and spaces for indentation.

4. Python 2 code indented with a mixture of tabs and spaces should be converted to using spaces exclusively.

5. When invoking the Python 2 command line interpreter with the -t option, it issues warnings about code that illegally mixes tabs and spaces. When using -tt these warnings become errors. These options are highly recommended!

###(ii) Imports

1. Do not pollute namespaces. So use variable names for your package, e.g.:
<pre><code>import numpy as np  
import pandas as pd</pre></code>


2. Imports should usually be on separate lines, e.g.:
<pre><code>Yes: import os as op_sys   
         import sys as s
No:  import sys as s, os as op_sys</pre></code>

3. It's okay to say this though:
<pre><code>from subprocess import Popen as pop, PIPE as pp</pre></code>

4. Imports are always put at the top of the file, just after any module comments and docstrings, and before module globals and constants.

##2. Whitespace in Expressions and Statements

###(i) Pet Peeves

1. Avoid extraneous whitespace in the following situations:  


Immediately inside parentheses, brackets or braces.  
<pre><code>Yes: spam(ham[1], {eggs: 2})  
No:  spam( ham[ 1 ], { eggs: 2 } )</pre></code>

Immediately before a comma, semicolon, or colon:  

<pre><code>Yes: 
if x == 4: print x, y; x, y = y, x  
No:  
if x == 4 : print x , y ; x , y = y , x</pre></code>

Immediately before the open parenthesis that starts the argument list of a function call:  
<pre><code>Yes: spam(1)  
No:  spam (1)</pre></code>

Immediately before the open parenthesis that starts an indexing or slicing:  
<pre><code>Yes: dict['key'] = list[index]  
No:  dict ['key'] = list [index]</pre></code>

More than one space around an assignment (or other) operator to align it with another.  

<pre><code>Yes:
x = 1
y = 2  
long_variable = 3
No:
x             = 1
y             = 2
long_variable = 3</pre></code>

###(ii) Other Recommendations

1. Always surround binary operators with a single space on either side.

2. Don't use spaces around the = sign when used to indicate a keyword argument or a default parameter value.

3. Compound statements (multiple statements on the same line) are generally discouraged.


##3. Comments

###(i) Always make a priority of keeping the comments up-to-date when the code changes!

1. Comments should be complete sentences. If a comment is a phrase or sentence, its first word should be capitalized, unless it is an identifier that begins with a lowercase letter (never alter the case of identifiers!).

2. If a comment is short, the period at the end can be omitted. Block comments generally consist of one or more paragraphs built out of complete sentences, and each sentence should end in a period.

3. You should use two spaces after a sentence-ending period.

4. When writing English, Strunk and White apply.

5. Python coders from non-English speaking countries: please write your comments in English, unless you are 120% sure that the code will never be read by people who don't speak your language.

###(ii)Block Comments

1. Block comments generally apply to some (or all) code that follows them, and are indented to the same level as that code. Each line of a block comment starts with a # and a single space (unless it is indented text inside the comment).

2. Paragraphs inside a block comment are separated by a line containing a single #.



###(iii)Inline Comments

1. Use inline comments sparingly.

2. An inline comment is a comment on the same line as a statement. Inline comments should be separated by at least two spaces from the statement. They should start with a # and a single space.

3. Inline comments are unnecessary and in fact distracting if they state the obvious. Don't do this:
<pre><code>x = x + 1                 # Increment x
But sometimes, this is useful:
x = x + 1                 # Compensate for border</pre></code>


###(iv) Code Header

1. When writing code specify a standard header block which tells others who has written the code and what functionality does it provide, e.g.,
<pre><code>#
# AUTHOR
# DATE
# BRIEF DESCRIPTION
#
# MODIFICATION DATE
#
</pre></code>

This should be followed by the initial author and by everyone else who modifies the code.


##5. Naming Conventions

###(i)Names to Avoid

1. Never use the characters 'l' (lowercase letter el), 'O' (uppercase letter oh), or 'I' (uppercase letter eye) as single character variable names.

2. In some fonts, these characters are indistinguishable from the numerals one and zero. When tempted to use 'l', use 'L' instead.



###(ii)Package and Module Names


Modules should have short, all-lowercase names. Underscores can be used in the module name if it improves readability. Python packages should also have short, all-lowercase names, although the use of underscores is discouraged.


###(iii)Class Names

Class names should normally use the CapWords convention.

###(iv)Exception Names

Because exceptions should be classes, the class naming convention applies here. However, you should use the suffix "Error" on your exception names (if the exception actually is an error).

###(v)Function Names

Function names should be lowercase, with words separated by underscores as necessary to improve readability.

###(vi)Function and method arguments

Always use self for the first argument to instance methods.  

Always use cls for the first argument to class methods.  

If a function argument's name clashes with a reserved keyword, it is generally better to append a single trailing underscore rather than use an abbreviation or spelling corruption. Thus class_ is better than clss. (Perhaps better is to avoid such clashes by using a synonym.)  

###(vii)Method Names and Instance Variables

Use the function naming rules: lowercase with words separated by underscores as necessary to improve readability.

###(viii)Constants

Constants are usually defined on a module level and written in all capital letters with underscores separating words. Examples include MAX_OVERFLOW and TOTAL.

