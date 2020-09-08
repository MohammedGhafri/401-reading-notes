# Regular Expressions in Python

if you want to start using them in your Python scripts, you have to import this module with the help of import:

`import re`

The re library in Python provides several functions that make it a skill worth mastering.

major methods in regular expression :

compile(), search(), findall(), sub() for search and replace, split(), and some more.


## Grouping in Regular Expressions

The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis () are called groups.

```
statement = 'Please contact us at: support@datacamp.com'
match = re.search(r'([\w\.-]+)@([\w\.-]+)', statement)
if statement:
  print("Email address:", match.group()) # The whole matched text
  print("Username:", match.group(1)) # The username (group 1)
  print("Host:", match.group(2)) # The host (group 2)

```

>>>Email address: support@datacamp.com

>>>Username: support

>>>Host: datacamp.com

### Greedy vs. Non-Greedy Matching

When a special character matches as much of the search sequence (string) as possible, it is said to be a "**Greedy** Match".


Summary table :

Character(s) |	What it does
-------------|----------------
.            |	A period. Matches any single character except the newline character.
^           |	A caret. Matches a pattern at the start of the string.
\A          |	Uppercase A. Matches only at the start of the string.
$            |	Dollar sign. Matches the end of the string.
\Z          |	Uppercase Z. Matches only at the end of the string.
[ ]	        |Matches the set of characters you specify within it.
\	    |∙ If the character following the backslash is a recognized escape character, then the special meaning of the term is taken.<br>∙ Else the backslash () is treated like any other character and passed through.<br>∙ It can be used in front of all the metacharacters to remove their special meaning.
\w  |	Lowercase w. Matches any single letter, digit, or underscore.
\W  |	Uppercase W. Matches any character not part of \w (lowercase w).
\s  |	Lowercase s. Matches a single whitespace character like: space, newline, tab, return.
\S  | Uppercase S. Matches any character not part of \s (lowercase s).
\d  |	Lowercase d. Matches decimal digit 0-9.
\D  |	Uppercase D. Matches any character that is not a decimal digit.
\t  |	Lowercase t. Matches tab.
\n  |	Lowercase n. Matches newline.
\r  |	Lowercase r. Matches return.
\b  |	Lowercase b. Matches only the beginning or end of the word.
+	|Checks if the preceding character appears one or more times.
*   |	Checks if the preceding character appears zero or more times.
?   |	∙ Checks if the preceding character appears exactly zero or one time.<br>∙ Specifies a non-greedy version of +, *
{ } |	Checks for an explicit number of times.
( ) |	Creates a group when performing matches.
< > |	Creates a named group when performing matches.


# shutil

def : The shutil module includes high-level file operations such as copying and archiving.

* Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as new special files with copyfile().

## Copying File Metadata

By default when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file to another, use copymode().

## Finding Files

The which() function scans a search path looking for a named file. The typical use case is to find an executable program on the shell’s search path defined in the environment variable PATH.