========================
PHP Level 1 (EDTECH-520)
========================

- Author: Christer Edwards
- Revision: 2013-03-06

Overview
========

- Development Environment
- Introduction
- Installation

=======================
Development Environment
=======================

Development Environment : Fedora
================================

{{:php:nutshell:slides:fedora-logo.png|Fedora}}

Login Information
=================

**username**: student

**password**: student

Browsers
========

{{:php:nutshell:slides:browsers-lancelot-462.png|Firefox}}

Terminal
========

{{:php:nutshell:slides:konsole-lancelot-462.png|Konsole}}

Editor
======

{{:php:nutshell:slides:kate-lancelot-462.png|kate}}

Platform Discussion
===================

 * Windows vs Linux vs Mac

Benefits of USB Environment?
============================

 * mobile
 * persistent
 * unique

Helpful Tools
=============

 * Gnote

Gnote Notes
===========

{{:php:nutshell:slides:gnote-lancelot-462.png|Gnote Notes}}

Questions : Environment
=======================

 * Questions?
 * Comments?

Development Environment : Lab
=============================

 * Become familiar with your development environment

   * Change your login password
   * Find your web browser(s) / text editor(s)
   * Launch Gnote Notes / Read 'Getting Started'
   * Customize your Desktop Appearance (Desktop Background, etc)
   * Logout / Login / Reboot / Shutdown / etc.


===================
Introduction to PHP
===================

PHP History
===========

 * Early Internet
 * C? Perhaps Perl?
 * 5 Versions since 1995
 * PHP 5: SQLite, SimpleXML, Improved OOP, Try/Catch

Advantages of PHP
=================

 * Fast
 * Easy
 * Widely Used / Popular

HTML Relationship
=================

 * Code Islands
 * Dynamic HTML Content

Interpreting vs Compiling
=========================

 * Opcodes
 * Code Cache
 * Garbage Collection

Output Control
==============

 * Code Island
 * Pure PHP
 * Buffering

Performance
===========

 * Rivals Perl and ASP
 * Continually Improving

Getting Help
============

If you have tried debugging and failed, don't fret–there are still support
options where you might find your solution.

Documentation
=============

 * Manual [http://www.php.net/manual/]

Mailing Lists
=============

 * php [http://www.php.net/mailing-lists.php]
 * uphpu [http://uphpu.org/mailman/listinfo/uphpu]

IRC
===

 * #php on irc.freenode.net - Global Support
 * #uphpu on irc.freenode.net - Local Support

Conferences
===========

 * O'Reilly's OSCON

User Groups
===========

 * uphpu [http://uphpu.org]

Getting Certified
=================

 * Zend Certification
 * MySQL Certification

Additional Reading
==================

 * http://www.php.net/manual
 * http://www.zend.com
 * http://www.phpbuilder.com
 * http://www.devshed.com

Questions : Introduction
========================

 * Questions?
 * Comments?

Introduction : Lab
==================

 * Visit the PHP Manual [1]

   * Search for a term from the book
 * Read about the mailing lists [2][3]

   * Subscribe to a mailing list
   * (php-general or uphpu)

 * [1] http://www.php.net/manual
 * [2] http://php.net/mailing-lists.php
 * [3] http://uphpu.org/mailing-lists-and-irc/

Installing PHP
==============

  * Beneficial to understand
  * Customization

Configuring Extensions
======================

  * ;extension=php_tidy.dll
  * extension=php_tidy.dll

Installing on Linux
===================

  * Package Manager
  * Compile Source

Installing Using Packages
=========================

  * yum
  * Add / Remove Software

Add / Remove Software
=====================

{{:php:nutshell:slides:apper.png|Add / Remove Software}}

LAMP (Linux Apache MySQL PHP)
=============================

The most common web-development environment is referred to as the "LAMP" stack.

Installation : Lab
==================

Verify functionality, create an 'index.php' in /home/student/Public/:

.. code-block:: php

	<?php phpinfo(); ?>

Visit: http://localhost/~student/


=====
Day 2
=====

===================
The PHP Interpreter
===================

Objectives : Interpreter
========================

 * Methods of executing PHP scripts.
 * Extending PHP

Running PHP Scripts
===================

 * Web Server
 * Command-Line Interpreter

Extending PHP
=============

 * Core
 * Bundled
 * PECL ("Pickle")
 * Third-Party
 * DIY

PEAR
====

 * PHP Extension and Application Repository

Abnormal Script Termination
===========================

 * You screwed up
 * PHP screwed up
 * Execution time
 * PHP Memory Limit

Questions : Interpreter
=======================

  * Questions?
  * Comments?

Interpreter
=================

 * Create a multi line CLI "Hello World" script
 * Create a multi line Web "Hello World" script
 * Install Mail_Mime from the PEAR Repository
 * Write an invalid script, run and repair


================
The PHP Language
================

Objectives : PHP Language
=========================

 * Become familiar with basic PHP syntax.
 * Use variables, arrays and other data types.
 * Create user-defined functions.
 * Use conditional logic.

The Basics of PHP
=================

.. code-block:: php

    <?php
        print "Hello World!";
    ?>

The Basics of PHP (cont.)
=========================

.. code-block:: php

    <?php print "Hello, "; print "world!\n"; ?>
    
    <?php echo "Hello, world!\n"; ?>
    
    <?php print("Hello, world!\n"); ?>

Variables
=========

Valid Variable Names

 * $myvar
 * $Name
 * $_Age
 * $_Age_
 * $Name91
 * $_Name91

Variables (cont.)
=================

Invalid Variable Names

 * $91
 * $1Name
 * $Name's

Variables : Examples
====================

.. code-block:: php

    <?php
        $name = "Paul";
        $age = 25;
        
        print "Hello, $name\n";
        print "Your are $age years old\n";
        
        // this won't print the way you might expect
        print 'Hello, $name. You are $age years old\n';
        print "\n";
    ?>

Variables (cont.)
=================

 * When calling variables, match name exactly
 * Surround variable in {}

Whitespace
==========

 * Spaces, tabs, blank lines don't matter

Heredoc
=======

.. code-block:: php

    <?php
      $mystring = <<<EOT
          This is some PHP text.
          It is completely free
          I can use "double quotes"
          and 'single quotes',
          plus $variables too, which will
          be properly converted to their values,
          you can even type EOT, as long as it
          is not alone on a line, like this:
      EOT;
    ?>

Heredoc Restrictions
====================

 * You can use anything you like; EOT is just an example.
 * You need to use %%<<<%% before the delimiter to tell PHP you want to enter heredoc mode.
 * Variable substitution is enabled, which means you need to escape dollar symbols if you don't want PHP to replace variables with their values.
 * You can use your delimiter anywhere in the text, but not in the first column of a new line.
 * At the end of the string, type the delimiter with no whitespace around it, followed by a semicolon.

Code Blocks
===========

.. code-block:: php

    <?php
    ?>

Commenting
==========

 * //
 * #
 * ``/* */``

Conditional Statements
======================

 * if
 * else
 * elseif

Conditional Statements : Examples
=================================

.. code-block:: php

    <?php
        $salary = 100000;
        
        if ($salary > 50000) {
            print "I'll take it!\n";
        } else {
            print "I'll keep looking...\n";
        }
    ?>

Conditional Statements : Example
================================

.. code-block:: php

    <?php
        $salary = 100000;
        
        if ($salary > 100000) {
            print "I'll take it!\n";
        } elseif ($salary > 75000) {
            print "I'll think about it...\n";
        } else {
            print "I'll keep looking...\n";
        }
    ?>

Conditional Statements : Example
================================

.. code-block:: php

    <?php
        $salary = 100000;
        
        if ($salary > 100000) {
            print "I'll take it!\n";
        } elseif ($salary > 80000) {
            print "I think I'll survive\n"
        } elseif ($salary > 75000) {
            print "I'll make do..\n";
        } elseif ($salary < 20000) {
            print "...are you serious!\n";
        }
    ?>

Case Switching
==============

 * If you find yourself with a list of elseif...else statements, use Case Switching

Case Switching : Example
========================

.. code-block:: php

    <?php
        $Name = 'Bob';
        switch($Name) {
        case "Jim":
            print "Your name is Jim\n";
            break;
        case "Linda":
            print "Your name is Linda\n";
            break;
        case "Bob":
            print "Your name is Bob\n";
            break;
        case "Sally":
            print "Your name is Sally\n";
            break;
        default:
            print "I don't know your name!\n";
        }
    ?>

Loops
=====

 * foreach
 * while
 * for
 * do...while

Loops (foreach) : Example
=========================

.. code-block:: php

    <?php
        foreach($array as $val) {
            print $val;
        }
    ?>

Loops (while) : Example
=======================

.. code-block:: php

    <?php
        $i = 1;
        while($i <= 10) {
            print "Number $i\n";
            $i = $i + 1;
        }
    ?>

Loops (for) : Requirements
==========================

 * Declaration
 * Condition
 * Action

Loops (for) : Example
=====================

.. code-block:: php

    <?php
          for ($i = 1; $i < 10; $i++) {
              print "Number $i\n";
          }
    ?>

Loops (do...while) : Example
============================

.. code-block:: php

    <?php
        $i = 11;
        do {
            print "Number $i\n";
        } while ($i < 10);
    ?>

Infinite Loops
==============

.. code-block:: php

    <?php
        while(1) {
            print "In loop!\n";
        }
    ?>

Loop Keywords
=============

 * continue
 * break

Loops Within Loops
==================

.. code-block:: php

    for () {
      for() {
        for() {
        }
      }
    }

Mixed Mode Processing
=====================

.. code-block:: php

    <?php
        if ($Age > 10) {
    ?>
    
    <p>Text goes here</p>
    <p>Text goes here</p>
    
    <?php
        }
    ?>

Including Other Files
=====================

 * include();
 * include_once();
 * require();
 * require_once();

functions
=========

 * shorter code
 * easier maintenance
 * less buggy
 * code reuse

functions : Example
===================

.. code-block:: php

    <?php
        $a = 27;
        $b = 55;
        
        // this function won't work as expected due to 'variable scope'
        function doMultiplication() {
            print $a * $b ."\n";
        }
        
        doMultiplication();
    ?>

functions : Example (cont.)
===========================

.. code-block:: php

    <?php
          // variables now available within proper scope
          function doMultiplication() {
              $a = 27;
              $b = 55;
              
              print $a * $b ."\n";
          }
          
          doMultiplication();
    ?>

Return Values
=============

 * You can return one value back from functions
 * Integer, string, Database connection, etc
 * Then exits the function immediately

Return Value : Example
======================

.. code-block:: php

    <?php
    
    function doMultiplication() {
        $a = 5;
        $b = 10;
        $result = $a * $b;
        
        return $result;
    
        print "extra stuff, after the function\n";
    }
    
    print doMultiplication() ."\n";
    
    ?>

Parameters
==========

 * Functions can accept input called Parameters
 * You can accept as many parameters as you need
 * You can process the parameters within the function

Parameters : Example
====================

.. code-block:: php

    <?php
    
    function doMultiplication($a, $b) {
        $total = $a * $b;
        return $total;
    }
    
    print doMultiplication(99, 52) ."\n";
    
    ?>

Default Parameters
==================

 * Assign default parameters
 * Allows you to require parameters, but not provide them each time

Default Parameters : Example
============================

.. code-block:: php

    <?php
    
    function doMultiplication($a, $b = 12) {
        $total = $a * $b;
        return $total;
    }
    
    print doMultiplication(99) ."\n";
    
    ?>

Variable Scope in Functions
===========================

 * variables declared outside of functions are considered //global//
 * variables declared inside of functions are considered //local//
 * global variables are available elsewhere in your scripts
 * local variables are not available outside functions

Overriding Scope with the GLOBALS Array
=======================================

 * Access global variables, even within functions
 * GLOBAL $foo;

Recursive Functions
===================

.. code-block:: php

    <?php
    function factorial($number) {
        if ($number == 0) return 1; // basic error checking
        return $number * factorial($number-1);
    }
    
    print factorial(8) ."\n";
    ?>

Questions : Language
====================

  * Questions?
  * Comments?

PHP Language : Lab
==================

Write a script using as many of the following elements as you can:

  * variable
  * heredoc
  * comments
  * conditional statement (if, else, elseif)
  * case switching
  * loops (foreach, while, for, do...while, continue, break)
  * function

=======================
Variables and Constants
=======================

Objectives : Variables & Constants
==================================

 * Become familiar with the range of data types in PHP.

Types of Data
=============

 * Boolean
 * String
 * Integer
 * Float

Boolean
=======

 * True / False
 * One / Zero
 * Most numbers are true, as are most strings

String
======

 * $a = "This is a string";
 * print $a[4];

Escape Sequences
================

 * \"
 * \'
 * \n
 * \t
 * \r
 * \$
 * %%\\%%

Integer
=======

 * $b = 4;
 * $c = 1000;
 * $d = 42;

Float
=====

 * 3.141592654
 * 2.1
 * 1.001

Automatic Type Conversion
=========================

 * PHP is loosely (weakly) typed
 * automatic conversion where possible
 * typecasting

Checking Whether a Variable is Set: isset()
===========================================

.. code-block:: php

    <?php
        if(isset($foo)) {
            print "$foo is defined.\n";
        } else {
            print "$foo is undefined.\n";
        }
    ?>

Superglobals
============

 * $_GET
 * $_POST
 * $_FILES
 * $_COOKIE
 * $_REQUEST
 * $_SESSION
 * $_SERVER
 * $_ENV
 * $GLOBALS

Using $_ENV and $_SERVER
========================

 * HTTP_REFERRER
 * HTTP_USER_AGENT
 * PATH_INFO
 * PHP_SELF
 * REQUEST_METHOD
 * QUERY_STRING

References
==========

 * two variables pointing to the same data

Constants
=========

 * immutable variables
 * no $ required
 * globally available

Preset Constants
================

 * FILE
 * LINE
 * FUNCTION
 * CLASS
 * METHOD

Mathematical Constants
======================

 * M_PI
 * M_PI_2
 * M_PI_4
 * ...

Arrays
======

 * Array
 * Associative Array
 * Multidimensional Array

Array
=====

.. code-block:: php

    <?php
        $fruits = array("Apples","Oranges","Pears");
        $size = count($fruits);
        print_r($fruits);
    ?>

Associative Arrays
==================

.. code-block:: php

    <?php
      $fruits = array("Apple"=>"red","Oranges"=>"orange","Pears"=>"green");
      var_dump($fruits);
    ?>

Multidimensional Array
======================

.. code-block:: php

   <?php
     $capitalcities['England'] = array("Capital"=>"London", 
         "Population"=>40000000);
     $capitalcities['Wales'] = array("Capital"=>"Cardiff", 
         "Population"=>50000000);
     $capitalcities['Scotland'] = array("Capital"=>"Edinburgh", 
         "Population"=>8000000);
   
     var_dump($capitalcities);
   ?>

Saving Arrays
=============

 * save arrays into files, sessions, etc.
 * serialize()
 * unserialize()
 * urlencode()
 * urldecode()

Questions : Variables
=====================

 * Questions?
 * Comments?

Variables / Data Types : Lab
============================

Write a script that uses:

 * boolean
 * string
 * float
 * integer
 * array (two types)

Make use of the isset() function.

=====
Day 3
=====

Overview
========

 * Review & Questions
 * Operators
 * HTML Forms
 * Security

PHP Language : Lab
==================

Write a script using as many of the following elements as you can:

 * variable
 * heredoc
 * comments
 * conditional statement (if, else, elseif)
 * case switching
 * loops (foreach, while, for, do...while, continue, break)
 * function

Variables / Data Types : Lab
============================

Write a script that uses:

 * boolean
 * string
 * float
 * integer
 * array (two types)

Make use of the isset() function.

=========
Operators
=========

Objectives : Operators
======================

Become familiar with the following types of PHP operators:

 * Arithmetic
 * Assignment
 * String
 * Comparison
 * Logical
 * Ternary

Arithmetic Operators
====================

 * ``+``
 * ``-``
 * ``/``
 * ``*``

Assignment Operators
====================

 * ``=``
 * ``=&``

String Operators
================

 * ``.``
 * ``.=``

Comparison Operators
====================

 * ``==``
 * ``===``
 * ``!=``
 * ``<>``
 * ``!==``
 * ``<``
 * ``>``
 * ``<=``
 * ``>=``

Incrementing and Decrementing Operators
=======================================

 * ``++$a``
 * ``$a++``
 * ``--$a``
 * ``$a--``

Logical Operators
=================

 * AND / &&
 * OR / ||
 * XOR
 * !

The Ternary Operator
====================

These are the same:

.. code-block:: php

    <?php
        $agestr = ($age < 16) ? 'child' : 'adult';
    ?>

    <?php
        if ($age < 16) {
            $agestr = 'child';
        } else {
            $agestr = 'adult';
        }
    ?>

The Execution Operator
======================

  * backticks (`)

.. code-block:: php

    <?php
        print `ls`;
    ?>

Operator Precedence and Associativity
=====================================

 * order of operations
 * generally left-to-right, with a few exceptions

Questions : Operators
=====================

 * Questions?
 * Comments?

Operators : Lab
===============

Include the following operators in your script:

 * Arithmetic (pg. 79)
 * String (pg .81)
 * Comparison (pg. 82)
 * Incrementing / Decrementing (pg. 84)
 * Logical (pg. 84)
 * Ternary (pg. 86)


