Part 1:




Part 2:

Reverse in Place
<div></div>
This is the original code for Reverse in Place:
<img width="338" alt="Screenshot 2023-01-26 at 2 18 53 PM" src="https://user-images.githubusercontent.com/43663025/214963555-b18202c1-bd02-45c8-b54e-46ee15a918f6.png">

This code will fail because it will replace all the values that it will eventially need to replace the ending with in the beginning. This code will not be able to make an accurate copy. To test whether this code will fail, one would need to write a test that involves a long array that the function needs to iterate through.

<div></div>

Test that passes:

This test has only one item `int[] input1 = {10};` so it passes the test
<div></div>
<img width="338" alt="Screenshot 2023-01-26 at 2 25 45 PM" src="https://user-images.githubusercontent.com/43663025/214964670-61f4ae9e-aa60-48e9-88bd-af86c9a598de.png">


New Test that Fails:

This test has a longer array as an imput. The input that fails is `int[] input1 = {3,4,5,6};` This test causes the function to produce the incorrect output
<div></div>
<img width="1145" alt="Screenshot 2023-01-26 at 2 16 36 PM" src="https://user-images.githubusercontent.com/43663025/214963163-4c77ad99-e52f-473f-9f0f-706b90d9a758.png">

Symptom:

Because of this error, one will see that the last term is copied once more to the first one, showing that it failed to reverse. This is because the code references a segment that has already been changed when it reaches the point where it needed to add items to the array.
<img width="367" alt="Screenshot 2023-01-26 at 2 37 59 PM" src="https://user-images.githubusercontent.com/43663025/214966587-db56f86c-0758-428c-a154-74a9f4bd067b.png">

Solution:

In order to solve this issue, one must create the copy of the array and then iterate through both arrays to replace the first item in the main array with the corresponding item from the end from the copy array. One should add this code to create a copy of the array. This would fix ones issue because it would allow one to iterate through the array without the potential for accidently duplicating the values at the end of the array into the beginning of the array.

       int[] copy = new int[arr.length];
       for(int i = 0; i < arr.length; i += 1) {
              copy[i] = arr[i];
       }
 
<div></div>
<img width="396" alt="Screenshot 2023-01-26 at 2 43 14 PM" src="https://user-images.githubusercontent.com/43663025/214967368-f7734e2b-330a-4ef4-93ef-42f41576968a.png">


Part 3:

I learned techniques that I can use int he future to debug my code when I have errors. I learned how to use Junit effectivley to ensure that my code ran smoothly. These techniques would be an incredibly valueable asset for me in my future.
