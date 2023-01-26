
Part 2

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

Solution:


