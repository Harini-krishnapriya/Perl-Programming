# Learn Perl with Me in 10 Days
This repository is designed to help you master the basics of Perl programming in just 10 days. Suitable for both beginners and experienced programmers.

## What You'll Learn

- **Day 1:** Introduction to Perl and Setting Up Your Environment
- **Day 2:** Basic Syntax and Variables
- **Day 3:** Control Structures and Looping
- **Day 4:** Subroutines and Functions
- **Day 5:** Working with Strings and Numbers
- **Day 6:** File Handling and I/O Operations
- **Day 7:** Regular Expressions and Pattern Matching
- **Day 8:** Data Structures: Arrays and Hashes
- **Day 9:** Modules and Packages
- **Day 10:** Final Project: Building a Simple Perl Application

## Introduction to Perl and Setting Up Your Environment
  - Perl is a high-level, interpreted programming language.
  - It is well known for its flexibility and powerful text-processing capabilities.
  - Perl runs on various platforms, including Unix/Linux, Windows, and macOS.
  - It is robust language used for a wide range of applications, including system administration, web development, and network programming.
### Setup Environment

To get started with Perl programming, you'll need a good Integrated Development Environment (IDE). We recommend using [Padre, the Perl IDE](https://padre.perlide.org/).

#### Why Padre?

- **User-Friendly**: Simple to download and use.
- **Quick Start**: Helps you start programming quickly and efficiently.
- **Features**: Provides a range of tools and features to streamline your development process.

#### Installation Steps

1. **Download**: Click [here](https://padre.perlide.org/) to download Padre.
2. **Install**: Follow the installation instructions provided on the website.
3. **Launch**: Open Padre and start coding!

By following these steps, you'll be set up with a powerful IDE that makes Perl programming easier and more enjoyable.

## Basic Syntax and Variables

Perl is known for its flexibility and expressive power. Here are some key elements of Perl's syntax:

### Comments

Comments in Perl begin with a `#` symbol and continue to the end of the line.

```perl
# This is a comment
```

### Print Statement

To print a statement, we use the `print` function.

### First Perl Program
Here’s a simple Perl program that demonstrates the basic syntax
```perl
#!/usr/bin/perl
use strict;
use warnings;

print "Hello, world.\n";
```
Save this file with a `.pl` extension, for example: `basic_program.pl`.
Now run the code, you will get Hello, world. as an output

#### Purpose of using `#!/usr/bin/perl`
- The line `#!/usr/bin/perl` at the beginning of a Perl script is called a shebang or hashbang.
- It's a special directive used in Unix-like operating systems (such as Linux and macOS) to indicate the path to the interpreter that should be used to execute the script.
- It makes the Perl script itself executable. Without the shebang line, you would typically need to explicitly call Perl followed by the script name to run it (e.g., perl script.pl). 

### Variables and Data Types
Perl supports several types of variables and data types.
#### Scalar Variables
Scalar variables in Perl are used to store single values, which can be a number, a string, or a reference. Scalar variables are prefixed with a dollar sign (`$`).
```perl
my $number = 42;         # An integer
my $string = "Hello!";   # A string
my $float = 3.14;        # A floating-point number
my $reference = \$number; # A reference to another variable
```
#### Arrays
Arrays store ordered lists of scalars. Array variables are prefixed with an `@` sign. Individual elements of an array are accessed using the `$` sign with the array name and the index in square brackets.
```perl
my @numbers = (1, 2, 3, 4, 5);       # An array of integers
my @words = ("apple", "banana", "cherry"); # An array of strings

# Accessing elements
print $numbers[0];  # Outputs 1
print $words[1];    # Outputs "banana"
```
**Note**: Arrays starts with index 0

#### Hashes
Hashes (associative arrays) store sets of key-value pairs. Hash variables are prefixed with a percent sign (`%`). Keys and values are scalars, and individual values are accessed using the `$` sign with the hash name and the key in curly braces.
``` Perl
my %fruit_colors = (
    "apple"  => "red",
    "banana" => "yellow",
    "grape"  => "purple"
);

# Accessing values
print $fruit_colors{"apple"};   # Outputs "red"
print $fruit_colors{"banana"};  # Outputs "yellow"
```
### Data Types
Perl supports various data types within its scalar, array, and hash variables:

#### 1. Numbers

- **Integers**: Whole numbers, positive or negative.
- **Floating-Point Numbers**: Numbers with decimal points.
- **Scientific Notation**: Numbers represented in scientific notation.
```perl
my $integer = 42;
my $float = 3.14159;
my $sci = 1.23e4;  # 1.23 x 10^4
```
#### 2. Strings
Strings are sequences of characters. They can be defined using single quotes (') or double quotes ("). Double quotes allow variable interpolation and special character sequences (escape sequences).
```Perl
my $single_quoted = 'Hello, World!';
my $double_quoted = "Hello, $name!";
my $escaped = "Line 1\nLine 2";
```
#### 3. References
References are scalars that "point" to other data types (arrays, hashes, subroutines, etc.). They are created using the backslash operator (`\`) and dereferenced using the appropriate symbol.
```perl
# Array reference
my @array = (1, 2, 3);
my $array_ref = \@array;

# Dereference
print $array_ref->[0];  # Outputs 1

# Hash reference
my %hash = (foo => 1, bar => 2);
my $hash_ref = \%hash;

# Dereference
print $hash_ref->{foo}; # Outputs 1
```
