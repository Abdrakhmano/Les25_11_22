### Task №1(7kyu)
A square of squares
You like building blocks. You especially like building blocks that are squares. And what you even like more, is to arrange them into a square of square building blocks!

However, sometimes, you can't arrange them into a square. Instead, you end up with an ordinary rectangle! Those blasted things! If you just had a way to know, whether you're currently working in vain… Wait! That's it! You just have to check if your number of building blocks is a perfect square.

Task
Given an integral number, determine if it's a square number:

In mathematics, a square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself.

The tests will always use some integral number, so don't worry about that in dynamic typed languages.

~~~
Examples
-1  =>  false
0  =>  true
3  =>  false
4  =>  true
25  =>  true
26  =>  false

isSquare (-1) // => false
isSquare   3  // => false
isSquare   4  // => true
isSquare  25  // => true
isSquare  26  // => false
~~~

[Task_link](https://www.codewars.com/kata/54c27a33fb7da0db0100040e/java)

#### Solution

~~~ Java
public class Square {
    public static boolean isSquare(int n) {
        if (Math.sqrt(n) % 1 == 0) {
            return true; // fix me!
        } else return false;
    }
}
~~~

#### Fav Solution

~~~ Java
public class Square {

    public static boolean isSquare(int n) {
        long s = Math.round(Math.sqrt(n));
        return s * s == n;
    }
}
~~~


### Task №2(6kyu)

Write simple .camelCase method (camel_case function in PHP, CamelCase in C# or camelCase in Java) for strings. All words must have their first letter capitalized without spaces.

For instance:
~~~
camelCase("hello case"); // => "HelloCase"
camelCase("camel case word"); // => "CamelCaseWord"
~~~
Don't forget to rate this kata! Thanks :)

[Task_link](https://www.codewars.com/kata/587731fda577b3d1b0001196/java)

#### Solution

~~~ Java 
public class Solution {

    public static String camelCase(String str) {
        var result = "";
        for (var word : str.split(" "))
        {
            result += word.isEmpty() ? "" : word.substring(0, 1).toUpperCase() + word.substring(1);
        }
        return result;
    }

}
~~~ 

#### Fav Solution 

~~~ Java
public class Solution {
    public static String camelCase(String str) {
        // your code here
        String[] strings = str.split(" ");
        StringBuilder stringBuilder=new StringBuilder();
        for (String string : strings) {
            if (string.length()>0){
                stringBuilder.append(string.replaceFirst(string.substring(0, 1), string.substring(0, 1).toUpperCase()));
            }

        }
        return new String(stringBuilder);

    }
}
~~~
