# Part 1:

Creating a webserver that continues to concatanate input onto a string and print the string out on the console. This code below creates a webserver and allows the user to continue to put strings into the url and print them out onto the console.

<img width="608" alt="Screenshot 2023-01-26 at 3 17 04 PM" src="https://user-images.githubusercontent.com/43663025/214971995-7d62e230-d79d-4482-ad02-973a4a06b8ae.png">


<img width="227" alt="Screenshot 2023-01-26 at 3 21 57 PM" src="https://user-images.githubusercontent.com/43663025/214972632-79aaf69e-ea75-4bc1-83a6-62c15e069f64.png">

If one were to add `add-message?s=Hello` the console, the code would create a new URI in Server.java. It would then call the handle request function. This goes into printing onto the console. This would create the varaible strings where the string will eventulayy be stored. (`String strings = "";`) This request would call the get path to check it if contains `add-message` and then continues to get the Query which appears after the ?. This is `s=Hello`. It will then split the query based on the equals sign, ensure that the left-side is an "s" and then concatanates "hello" to strings. It then returns strings and prints on the console.

<img width="415" alt="Screenshot 2023-01-26 at 3 18 27 PM" src="https://user-images.githubusercontent.com/43663025/214972176-dc881179-b007-44cb-997a-abde2fe9520e.png">

If one were to add `add-message?s=My%20name%20is%20Mihir` the console, the code would create a new URI in Server.java. It would then call the handle request function. The varaible strings has already been created and contains the word "Hello" and a new line character inside of it. This request would call the get path to check it if contains `add-message` and then continues to get the Query which appears after the ?. This is `s=My%20name%20is%20Mihir`. It will then split the query based on the equals sign, ensure that the left-side is an "s" and then concatanates "My name is Mihir" to strings. It then returns strings with the "Hello" and new line and prints on the console.

<img width="555" alt="Screenshot 2023-01-26 at 3 27 23 PM" src="https://user-images.githubusercontent.com/43663025/214973320-4b8cf644-56a3-4581-9a6f-268066b04853.png">

# Part 2:

Reverse in Place
<div></div>
This is the original code for Reverse in Place:
<div></div>

       static void reverseInPlace(int [] arr) {
              for(int i = 0; i < arr. length; i += 1) €
                     arr[il = arr[arr. length - i - 1];
              }
       }

This code will fail because it will replace all the values that it will eventially need to replace the ending with in the beginning. This code will not be able to make an accurate copy. To test whether this code will fail, one would need to write a test that involves a long array that the function needs to iterate through.

<div></div>

Test that passes:

This test has only one item `int[] input1 = {10};` so it passes the test
<div></div>

       @Test
       public void testReverseInPlace2 () {
              int [] input1 = {10} ;
              ArrayExamples.reverseInPlace(input1);
              assertArrayEquals (new int []{10), input1) ;
       }

New Test that Fails:

This test has a longer array as an imput. The input that fails is `int[] input1 = {3,4,5,6};` This test causes the function to produce the incorrect output
<div></div>
<img width="1145" alt="Screenshot 2023-01-26 at 2 16 36 PM" src="https://user-images.githubusercontent.com/43663025/214963163-4c77ad99-e52f-473f-9f0f-706b90d9a758.png">

Symptom:

Because of this error, one will see that the last term is copied once more to the first one, showing that it failed to reverse. This is because the code references a segment that has already been changed when it reaches the point where it needed to add items to the array.

<img width="367" alt="Screenshot 2023-01-26 at 2 37 59 PM" src="https://user-images.githubusercontent.com/43663025/214966587-db56f86c-0758-428c-a154-74a9f4bd067b.png">

       static void reverseinPlace(int[] arr) {
              for(int 1 - 0; 1 < arr. length; 1 += 1) €
                     arr[i] = arr[arr. length - i - 1];
              }
              System.out•println(Arrays.toString(arr));
       }

Solution:

In order to solve this issue, one must swap the indexes without replacing the values that are inside. To do this, one should make a copy of the index before switching. This would allow the swap to happen sucessfully.


       static void reverseinPlace(int[] arr) {
              for (int i = 0; i < arr.length / 2; i++) {
                     int copy = arr[i];
                     arr[i] = arr[arr.length; i -= 1];
                     arr[arr.length - 1 - i] = copy;
              }
              System.out.println(Arrays. toString(arr)) ;
       }


# Part 3:

I learned techniques that I can use int he future to debug my code when I have errors. I learned how to use Junit effectivley to ensure that my code ran smoothly. These techniques would be an incredibly valueable asset for me in my future.
