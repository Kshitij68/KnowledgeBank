1. Java forces you to properly write the types of data structure
2. Filename must be same as the public class you define in the file
3. What is the benefit of compilation
   1. Early detection of errors
   2. Faster program execution
   3. Turn java code into language that JVM can understand, i.e. byte code
4. Every java program must define a class, and all code is inside a class
5. Every java program must have a function called `public static void main(String[], args)`
   1.  `public` which is one of security features in Java. The following security features are provided by Java:-
      1. public
      2. protected
      3. private
   2. `static` tells that this method is part of the class, but a method for any one instance of class
      1. e.g. we can invoke `Hello.main(parameters)`
   3. `void` tells that Java does not have a types
6. Find length
   1. String -> use `my_string.length()` -> Used as a function
   2. Arrays -> use `my_length.length` -> Used as a property
7. `new` Creating new object
8. You can directly return the value in function without type declaring it first.
   1. e.g. `return array.length;`
9. `contains` : To see if a string contains a given substring
   1. `"ABC".contains("A")`
10. `List<String> L = new ArrayList<String>();` : This creates a dynamic list (similar to list in python)
11. You have to import Data Structures in Java
    1.  java.utils.HashSet
        1.  HashSet<Character> unique = new HashSet<Character>();
        2.  unique.add(s.charAt(i));
    2.  java.utils.HashMap
        1.  HashMap<Character, Integer> hm = new HashMap<>();
        2.  hm.put(ch,hm.getOrDefault(ch,0)+1);
12. Difference between `int/char` vs `Integer/Character`
    1.  int/char are primitive data type
    2.  Character/Integer is class that contains many in-built methods
13. Iterate over string 
    1.  for (int i = 0; i < s.length(); i++) { s.charAt(i); }
14. Strings
    1.  Iterate over Strings
        1.  for (int i = 0; i < s.length(); i++) { s.charAt(i); }
    2.  Compare two strings
        1.  string1.equals(string2)