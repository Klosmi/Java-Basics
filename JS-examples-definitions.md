__[◀️ go back](https://github.com/Klosmi/Java-Basics/blob/main/README.md#java-language-basics)__

## [Functions](https://www.learnjavaonline.org/en/Functions)
Creating a functions
- we have to specify the __return type__ of the function: some returns a value, some returns nothing.

<br>

#### __[`void`](https://www.w3schools.com/java/ref_keyword_void.asp#:~:text=The%20void%20keyword%20specifies%20that,not%20have%20a%20return%20value.)__ + `nameOfTheFunction(parameter)` + `{ }` →    
The `void` keyword specifies that a method should not have a return value. 

<br>

#### __[`main()`](https://www.geeksforgeeks.org/java-main-method-public-static-void-main-string-args/)__    
is the entry point to our program.   
Whenever using `main`, the `main` gets called and the code inside it will be executed.

<br>

#### __[class](https://www.javatpoint.com/object-and-class-in-java)__    
a container of one or more related functions.   
  - A __class__ is a template used to create objects and to define object data types and methods.    
  - Every Java program has atleast 1 class that contains the `main` function.  
  - PascalNamaingConverntion (classes start with a Capital letter)

<br>

#### __[methods](https://www.javatpoint.com/method-in-java)__: 
is a block of code or collection of statements or a set of code grouped together to perform a certain task or operation. It is used to achieve the reusability of code.    
  - camelNamingConvention (firstletter is lowercase)
  - a __method__ is a function that is part of a class. 

```
class Main {
  void main() {

  }
}
```

<br>

#### __[access modifiers](https://www.geeksforgeeks.org/access-modifiers-java/)__   
in Java specifies the accessibility or scope of a field, method, constructor, or class.   
some modifieres: public, private, etc.

```
public class Main {         //← main class
  public void main() {      //← main method

  }
}

```

<br>

#### __[package](https://www.javatpoint.com/package)__    
A package in Java is used to group related classes. Think of it as a folder in a file directory. We use packages to avoid name conflicts, and to write a better maintainable code. Packages are divided into two categories:   

Built-in Packages (packages from the Java API).  
User-defined Packages (create your own packages)   

  - the base package is the domain name of your the company:  `com.whatever`
  - it is just a way to create a namescpace for your classes
  - every classes that we are creating will belong to that `com.whatever` package

- all Java file has a `.java` extension

- `//` comment

<br>

#### [`PrintStream`](https://www.programiz.com/java-programming/printstream#:~:text=Unlike%20other%20output%20streams%2C%20the,throw%20any%20input%2Foutput%20exception.):     
converts the primitive data (integer, character) into the text format instead of bytes.

- eg.:   
  *print out a line*
  ```
    package com.tuto;                               //← our package

    public class Main {
        public static void main(String[] args) {

            System.out.println("Hello world!");     //← prin line
        }
    }
  ```

<br>

#### __[compilation](https://www.theserverside.com/definition/Java-compiler)__: 
a Java compiler is a program that takes the text file work of a developer and compiles it into a platform-independent Java file. 
  - we can RUN the java file in Temrinal:
    ```
    javac Main.java           // press Enter

    ls                        // look at the content of the folder

    Main.class  Main.java     // Main.class is a new file a bytecode representation of the Java file

    cd ..
    cd ..                     // we are inside the source folder

    java com.tutorial.Main    // invoke JVM + the path to our Main Java + Enter

    Hello World!              // program is executed  
    ```

- __*out* folder__: result of the Java compilation 

- __JRE__: Java Runtime Environment

- __JVM__: Java Virtual Machine (is the software component of JRE). what it does, is that it takes the Java bytecode and translates it to the native code for the underlyung operating system. (That is why Java program is portable = platform independent)

<br>

## [Data Types](https://www.javatpoint.com/java-data-types) 
Data types specify the different sizes and values that can be stored in the variable. There are two types of data types in Java:

  - *Primitive data types*:    
  The primitive data types include boolean, char, byte, short, int, long, float and double.

  - *Non-primitive data types or Reference types*:    
  The non-primitive data types include Classes, Interfaces, and Arrays.


#### [variables](https://www.javatpoint.com/java-variables)

 - __[int](https://www.javatpoint.com/int-keyword-in-java)__:   
    - *__intiger__*
    - it can also be used with methods to return integer type values
    - is a primitive data type. 
    - it is used to declare variables. 
    + `int identifier = 30;`  ← here we intitalized identifier varible with the value 30
    ```
    package com.tuto;

    public class Main {
        public static void main(String[] args) {
            int age = 30;
            age = 35;                           //← change the value
            System.out.println(age);            //← printing the value of the age variable
        }
    }
    ```
    - we can initialize multiple variable in the same line (bad practice, becasue it's ugly): using a comma __`,`__ to declare multiple variables. `int myVar = 30, otherVar = 10;`
    - best practice: declare one variable in each line (*no comma is needed*)

```
      package com.tuto;

      public class Main {
          public static void main(String[] args) {
              int age = 30;
              temperature = 20;
              age = 35;                           //← change the value
              System.out.println(age);            //← printing the value of the age variable
          }
      }
```

<br> 

  #### [Primitive types](https://www.baeldung.com/java-primitives#:~:text=2.-,Primitive%20Data%20Types,about%20memory%20management%20in%20Java):
  to store simple values


    - byte :  1 byte of the memory and can take -128, 127 numbers
    - short:  2 bytes of the memory and can take -32K, 32K numbers
    - int:    4 bytes of the memory and can take -2Billion, 2Billion numbers
    - long:   8 bytes of the memory and large numbers

  <br>
      - float:  4 bytes of the memory
      - double: 8 bytes of the memory

  <br>

      - char:   2 bytes of the memory: A,B,C,...`

  <br>
      - boolean: 1 byte, true/false 

  - eg.:   

  *Using different variables*

```
  package com.tuto;

  public class Main {
      public static void main(String[] args) {
          byte age = 30;                    // byte is enough for age
          int viewsCount = 123_456_789;     // _ separates digits to make it more readable
          long watchCounts = 3_123_456_789L //error that it's too big number, even if we use the long type. We use L
          float price = 10.99F;              // error, Java thinks its double type, we give F (float)
          char letter = 'A';
          boolean isEligible = true;
      }
  }
```

<br>

#### [Reference types](https://www.geeksforgeeks.org/types-references-java/):
to store complex objects (date, mail messages, etc.)
- we have to use the `new` keyword, to allocate memory for the variable
- creating object: `Date today = new Date();` ← `today` is an instance of the `Date();` class. `Date()` is the blueprint of creating objects.
- an object is an instance of a class: `obejct` + `.` `member`.   
Eg. `today.getTime()`
- `Strings` are reference types

*Using different variables*
*Print out the `Data` object: `System` is a class, followed by `.` operator to access System class's member. After the `out` is a field. Type of `out` filed is `PrintStream`, it is an other class in Java. After `.` and `println()` finction. In the `()` we pass the Date object.*     

*So it looks like this `System.out.println(today);`*    
💡 *Use `sout` shortcut to print the line above.*
```
  package com.tuto;

  import java.util.Date;          // we use Date reference type, so Java imports the Date class from the util package

  public class Main {
      public static void main(String[] args) {
          byte age = 30;
          Date today = new Date();  // creating a Date() class
          now.
          today.getTime()
      }
  }
```

<br>

#### [Primitive vs. Reference types](https://java-programming.mooc.fi/part-5/3-primitive-and-reference-variables#:~:text=Variables%20in%20Java%20are%20classified,information%20related%20to%20that%20variable.)

The difference between these two types are also in the memory management.

- eg.:    
  *`x = 1` and `y = x`. When we change the value of `x`, `y` doesn't change. Because `x` is in a different part of the memory than `y` they are independent from eachother*
  ```
  package com.tuto;

  public class Main {
      public static void main(String[] args) {
          byte x = 1;
          byte y = x;
          x = 2;
          System.out.println(y);
      }
  }


  // output: 
  // 1
  ```
  *We use reference types*
  *We use the `Point` class, it is deifnied in the package → `import java.awt.*;`. We create `point1` and a `point2`. The `point2` varibale is set to `point1`.*

  *When JRE executes `Point point1 = new Point(x:1, y:1);`, it allocates a memory to store the `Point(1, 1)` object.*

  *Then Java allocates a separate part of the memory and attaches the `Point(1, 1)` object's memory label (address) to that separate part of the memory location.*   

  *In that location, it stores the address of the `Point(1, 1)` object.*

  *So the variable is holding the address and not the actual object.*

  *In primitive type a varibale's value is stored in the same memory location. → That is the key difference between primitve and reference type.*
  ```
  package com.tuto;

  import java.awt.*;

  public class Main {
      public static void main(String[] args) {
          Point point1 = new Point(x:1, y:1);
          Point point2 = point1;
          point1.x = 2;
          System.out.println(point2);
      }
  }


  // expected output:
  //java.awt.Point[x=2,y=1]
  ```

<br>

#### __[Strings](https://www.javatpoint.com/java-string)__  

String literal = string value →"Hello World" from the  `System.out.println("Hello World") 

- `String`s are inmutable = you can't change them. Any method that modify a string returns a __new__ string object (copy).

- eg.:   
  *We define a String variable `message`. `String` is a class. Since we are dealing with a reference type, we instantiate the `message` variable using the `new` operator. But we don't have to write `new String( "Hello World");` if we only write `String message = "Hello World";` will be the same, it is just a shortest way.*    
  *Also we concatenated the "Hello World" + "!!"*
  ```
  package com.tuto;

  import java.awt.*;

  public class Main {
      public static void main(String[] args) {
          String message = "Hello World" + "!!";   //← the original new String( "Hello World!");
          System.out.println();
      }
  }

  // "Hello World!!"
  ```
  *Since `String` is a class, we can access using the __`.`__ operator.*
  ```
  public class Main {
    public static void main(String[] args) {
        String message = "Hello World" + "!!"; // this is the original new String( "Hello World");

        System.out.println(message.endsWith("!!"));       //← message. + methods we can add, eg. endsWith()
        System.out.println(message.replace(target:"!", replacement:"*"));     // target and replacement are parameters, "!" and "*" are argeuments (values) 
    }
  }

  // Hello World**
  // true
  ```

<br>

#### __[Escape sequences](https://www.geeksforgeeks.org/escape-sequences-in-java/)__
    A character with a backslash (\) just before it is an escape sequence or escape character. 

__`\`__   
Escapes the `" "`
- eg.:   
*using the backslash \ when using quotes*
```
public class Main {
    public static void main(String[] args) {
        String message = "Hello \"You\"";
        System.out.println(message);
    }
}

//Hello "You"
```

__`\\`__     
Escapes the backslash \  
*How to escape the backslash \, when writing `c:\\Wondows\...?*
```
public class Main {
    public static void main(String[] args) {
        String message = "c:\\Windows\\...";  //← using double \\
        System.out.println(message);
    }
}

// c:\Windows\...
```
__`\n`__:   
new line 

```
public class Main {
    public static void main(String[] args) {
        String message = "c:\nWindows\\...";
        System.out.println(message);
    }
}

//c:
//Windows\...
```
__`\t`__    
adds a tab


#### __[Arrays](https://www.geeksforgeeks.org/arrays-in-java/)__
we use arrays to store a list of items. 

- arrays in Java have a fixed size: we can't add or remove

- eg.:    
__old way of intitalizing an Array.__   
*Creating an array.*
*Arrays are reference type → we use the `new` operator.*
*`new int[define the size of the array]`*
*We have to use a class `Arrays` to see the actual array.*
```
package com.tuto;

import java.util.Arrays;                  //← because we use the Arrays class

public class Main {
    public static void main(String[] args) {
        int[] numbers = new int[5];
        numbers[0] = 1;                   //← intitalizing the Array's indexes
        numbers[1] = 2;
        System.out.println(Arrays.toString(numbers));     //← Arrays. method (here it turns the values into strings)
    }
}

// [1, 2, 0, 0, 0]
```

-eg.:   
❗️ __A simpler, newer way to initialize Arrays.__   
*Using `{ }`*
```
package com.tuto;

import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = { 2, 3, 5, 1, 4 };
        System.out.println(numbers.length);
    }
}

// 5    //hte length of our string
```
*Sorting*  
```
package com.tuto;

import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = { 2, 3, 5, 1, 4 };
        Arrays.sort(numbers);                   //← calling Arrys with the sort method.
        System.out.println(Arrays.toString(numbers));
    }
}

// [1, 2, 3, 4, 5]
```

<br>

#### __[Multidimensional Arrays](https://www.geeksforgeeks.org/multidimensional-arrays-in-java/)__    
Array of arrays.   
Data in multidimensional arrays are stored in tabular form (in row major order).

- useful of creating matrixes
  - eg.:  
  __*2D array*__  
  *The first[] defines the row, the second[] defines the columns.*
  *We have to use the `deepToString()` method in case of multidimensional arrays.*   
  ```
  package com.tuto;

  import java.util.Arrays;

  public class Main {
      public static void main(String[] args) {
          int[][] numbers = new int[2][3];          //← 2 rows and 3 columns
          numbers[0][0] = 1;
          System.out.println(Arrays.deepToString(numbers));
      }
  }

  [[1, 0, 0], [0, 0, 0]]
  ```
  __*3D array*__
  ```
  package com.tuto;

  import java.util.Arrays;

  public class Main {
      public static void main(String[] args) {
          int[][][] numbers = new int[2][3][2];
          numbers[0][0][0] = 1;
          System.out.println(Arrays.deepToString(numbers));
      }
  }

  // [[[1, 0], [0, 0], [0, 0]], [[0, 0], [0, 0], [0, 0]]]
  ```

  ❗️ __Simple way__
  ```
  package com.tuto;

  import java.util.Arrays;

  public class Main {
      public static void main(String[] args) {
          int[][] numbers = {{1,2,3},{4,5,6}};
          System.out.println(Arrays.deepToString(numbers));
      }
  }

  // [[1, 2, 3], [4, 5, 6]]
  ```

<br>

#### __[Constants](https://www.javatpoint.com/java-constant)__     
Constant is a value that cannot be changed after assigning it. 
- Starts with Capital letter

- eg.:   
*We don't want to allow to overrite the variable PI, so we make it as a Constant.*
```
package com.tuto;

public class Main {
    public static void main(String[] args) {
        final float PI = 3.14F;
    }
}
```

<br>

#### __[Arithmetic Expression](https://www.webucator.com/article/how-to-write-an-arithmetic-expression-in-java/#:~:text=An%20arithmetic%20expression%20in%20Java%20is%20a%20sequence%20of%20numeric,arithmetic%20expression%20is%20a%20number.)__    

__+__    
__-__   
__*__    
__/__ 
__%__   

- eg.:   
 *A simple addition*
 ```
 package com.tuto;

 public class Main {
      public static void main(String[] args) {
        int result = 10 + 3;
        System.out.println(result);
      }
 }
 
 // 10
 ```
*The division of whole numbers gives the result of a whole number. `10 / 3` result is `3`.*
 ```
 package com.tuto;

 public class Main {
      public static void main(String[] args) {
        int result = 10 / 3;
        System.out.println(result);
      }
 }
 
 // 3
 ```
 *To have a float number we have to convert the numbers into `double` or `float`.*
 ```
 package com.tuto;

 public class Main {
      public static void main(String[] args) {
        double result = (double)10 / (double)3;
        System.out.println(result);
      }
 }
 
 // 3.3333333333333335
 ```
 *Increment the `int x` by 1.*
 ```
 package com.tuto;

  public class Main {
      public static void main(String[] args) {
        int x = 1;
        x++;
        System.out.println(x);
      }
  }

// 2
```

*First `y` takes the value of `x`, so it's `1`. __Then__ `x` increment by `1`, so `x` becomes `2`*
```
package com.tuto;

public class Main {
    public static void main(String[] args) {
       int x = 1;
       int y = x++;                  
       System.out.println(x);
       System.out.println(y);
    }
}

// 2
// 1
```
*Lets change and place the `++` to the left side of the `x`. We get a different result.*   
*Now, first `x` incremented by `1`, so it becomes `2`, and __then__ `y` takes the value of `x`, so it becomes `2`.*
```
package com.tuto;

public class Main {
    public static void main(String[] args) {
       int x = 1;
       int y = ++x;                     
       System.out.println(x);
       System.out.println(y);
    }
}

// 2
// 2
```
*Augment `x` by more than `1`, like `2`.*   
*Augmented or compound assignment operators*  
*`x += 2`*
```
package com.tuto;

public class Main {
    public static void main(String[] args) {
       int x = 1;
       x += 2;                  // its the same x = x + 2;
       System.out.println(x);
    }
}

// 3
```

<br>

#### __[Casting](https://www.javatpoint.com/type-casting-in-java)__
Converts a data type into another data type in both ways manually and automatically.

__Widening Casting or Implicit casting__

- no data loss

- ther order is:   
  __byte → short → int → long → float → double__ 

- eg.:   
  *We have a 2 different types of values: `short x` and an `int y`.*

  *What happens, is one of the type converts to the other. Since `short` has 2bytes, and `int` has 4 bytes, so the value stored in the `short` variable can be stored in the `int` variable.*
  ```
  package com.tuto;

  public class Main {
      public static void main(String[] args) {
        short x = 1;
        int y = x + 2;
        System.out.println(y);
      }
  }

  // 3
  ```
 __Narrowing Casting (Explicit Casting)__

 - eg.:
 *We want to see `3` as a result. but we have a `double` and and an `int`. We have to __explicityl cast__ the result.*    
 *We have to  __cast__ `x` to an `int` like this: `int y = (int)x + 2`    

  ```
  package com.tuto;

  public class Main {
      public static void main(String[] args) {
        double x = 1.1;
        int y = (int)x + 2;
        System.out.println(y);
      }
  }

  // 3
  ```

__`parese.Int`__

  Casting can happen between compatible type. A string can't cast with a number. But with the `Integer` class we can use the `parseInt()` method, which turns a `String` `"1"` into number.   
  - eg.:   
  *Using the `parseInt()` to turn a String into an `int`.*
  ```
  package com.tuto;

  public class Main {
      public static void main(String[] args) {
        String x = "1";
        int y = Integer.parseInt(x) + 2;
        System.out.println(y);
      }
  }
  ```

#### __[Math Class](https://www.javatpoint.com/java-math)__   
Math class provides several methods to work on math calculations like min(), max(), avg(), sin(), cos(), tan(), round(), ceil(), floor(), abs() etc.   

```
package com.tuto;

public class Main {
    public static void main(String[] args) {
        int result1 = Math.round(1.1F);                      // round
        int result2 = (int)Math.ceil(1.1F);                  // Cast to an int. Ceil of a number is the smallest int which is greater or equal to the number.
        int result3 = (int)Math.floor(1.1F);                 // Cast to an int. Floor of a number is the largest int, that is smaller or equal to the number.
        int result4 = Math.max(1, 2);                        // Returns the greater number.
        int result5 = (int)Math.round(Math.random() * 100);  // Random num between 0 - 1. Returns a Double.
        int result6 = (int)(Math.random() * 100);
        
        System.out.println(result1);
        System.out.println(result2);
        System.out.println(result3);
        System.out.println(result4);
        System.out.println(result6);
    }
}

// 1
// 2
// 1
// 2
// 96
```

<br>

#### __[Formatting Numbers](https://zetcode.com/java/numberformat/#:~:text=NumberFormat%20is%20a%20Java%20class,according%20to%20a%20specific%20locale.)__    
NumberFormat allows us to round values, set decimal separators, set the number of fraction digits, or format values according to a specific locale.

- eg.:    
  *Using the `NumberFormat` class, we can not create an instance of the NumberFromat class, because it is "abstract": so `NumberFormat x = new NumberFromat()` will throw an error.* 

  *BUT, __we can use__ `NumberFormat`'s __`factory`__ __methods__ ❗️ (like `NumberFormat.getCurrencyInstance()`), because they create an instance of the NumberFormat class, and return it.*

  *It is called factory method, because it creates new objects.*

  *We store the `NumberFormat.getCurrencyInstance();` value in a variable of type `NumberFormat` (eg. `NumberFormat currency = NumberFormat.getCurrencyInstance();`).*

  *The `currency` objact has a method for `format`ting  values. We call that method and pass a  value `currency.format(1234567.891);`. Since the `foramt` method returns a `String` represenatation of the number, we store it in a String variable.*

  *
  ```
  package com.tuto;

  import java.text.NumberFormat;
  import java.util.Locale;

  public class Main {
      public static void main(String[] args) {
        NumberFormat currency =  NumberFormat.getCurrencyInstance(Locale.FRANCE);
        String result = currency.format(1234567.891);
        System.out.println(result);
    }
  }

  // 1 234 567,89 €
  ```
  *Formatting to percent %.*
  ```
  package com.tuto;

  import java.text.NumberFormat;

  public class Main {
      public static void main(String[] args) {
        NumberFormat percent = NumberFormat.getPercentInstance();
        String result = percent.format(0.1);
        System.out.println(result);
      }
  }

  // 10%
  ```
  *We can chain this example into one line, it is the method chaining.*
  ```
  package com.tuto;

  import java.text.NumberFormat;

  public class Main {
      public static void main(String[] args) {
        String result = NumberFormat.getPercentInstance().format(0.1);
        System.out.println(result);
      }
  }
  ```

#### __[Reading Input](https://www.javatpoint.com/how-to-get-input-from-user-in-java)__
Java `Scanner` class allows the user to take input from the console.

- eg.:   
*Using the `Scanner` class, and we create a `scanner` object, and we instantiate `new Scanner()`*   
*Inside the we specify `new Scanner(where we read the data)` → `System.in` (not out) → `Scanner scanner = new Scanner(System.in);`*     
*The `scanner` object has methods for reading data, the all start with `.next...`.*
```
package com.tuto;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        System.out.print("Age: ");
        byte age = scanner.nextByte();
        System.out.print("You are " + age);       // to have the same line, we just use `print` and not `println`
    }
}

// Age:  20
// "You are 20"
```
*Input a String.*
```
package com.tuto;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);       
        System.out.print("Your name is: ");
        String name = scanner.next();
        System.out.println("You are " + name);
    }
}

// Your name is: John 
// "You are John"
```
*To have a full name, eg. John Doe, we need to combine the so called tokens. John is a token, space is a token, Doe is a token.*    
*There isa method for this: `scanner.nextLine()`*   
```
package com.tuto;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Your full name is: ");
        String name = scanner.nextLine().trim();        /← to avoid whit spaces before and after the name
        System.out.println("You are " + name);
    }
}

// Your full name is: John Doe
// "You are John Doe"
```
