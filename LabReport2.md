# Lab Report 2
## Part 1
Code for StringServer.java:  
<img width="1131" alt="Screen Shot 2023-01-28 at 2 50 30 PM" src="https://user-images.githubusercontent.com/110351703/215294685-679ab985-b608-4660-a101-e4750206e016.png">
I also used the Server.java file provided during Lab 2.  

Screenshot #1:  
<img width="472" alt="Screen Shot 2023-01-28 at 2 48 03 PM" src="https://user-images.githubusercontent.com/110351703/215294711-5489aaf8-9329-4658-b2ba-42edd7b5961d.png">  
For this screenshot, the handleRequest method and main method are called when the code is compiled and run.
Since the path is /add-message, it will go to the else-if statement and then check for what comes after /add-message.
Since s=Hello comes after, it will go into the next if-statement and update the whole string by creating a new line and adding "Hello". 

Screenshot #2:  
<img width="474" alt="Screen Shot 2023-01-28 at 2 52 15 PM" src="https://user-images.githubusercontent.com/110351703/215294728-867b6ae6-7c33-49be-9dbe-f2148154424f.png">  
Similarly to the first screenshot, the handleRequest method and the main method are also called for this screenshot.
The first portion of the path is the same, so it will skip the first if statement in the handleRequest method and go to the else-if statement because the
path is /add-message. After it checks for the next portion in the URI, it will continue to the next if-statement within the else-if statement and update the string.
A new line is added and "HelloWorld" is concatenated to the string.  
## Part 2 
Failure inducing input: 
```
@Test
  public void testReverseInPlaceArray2() {
    int[] input1 = {4, -1, 5, 5, 0};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{0, 5, 5, -1, 4}, input1);
  }
  ```
  Non-failure inducing input:
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```  
Non-symptom:  
<img width="441" alt="Screen Shot 2023-01-28 at 5 15 23 PM" src="https://user-images.githubusercontent.com/110351703/215298666-758e6f60-de05-4e5b-bb88-422ad3ec93c4.png">

Symptom:
  <img width="1005" alt="Screen Shot 2023-01-28 at 5 14 57 PM" src="https://user-images.githubusercontent.com/110351703/215298653-02284530-dc4b-4937-b035-8b6b3cc6a4da.png">  

Original Code:  
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```  

Altered Code:
```static void reverseInPlace(int[] arr) {
    int temp;
    for(int i = 0; i < arr.length / 2; i += 1) {
      temp = arr[i];
      arr[i] = arr[arr.length - i -1];
      arr[arr.length - i - 1] = temp;
    }
  }
```  
This altered code ensures that the second half of the array is also getting updated so as the first half is being swapped with the second half, the second half is also being swapped with the first half.
## Part 3
Something new that I learned in week 2 was about web servers. I didn't know that I could host them from my own computer. I hadn't known anything about ports or how to make a web server, so creating one that others could access from their own laptops was pretty cool. 
