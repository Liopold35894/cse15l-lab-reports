# **Servers and Bugs**
First we're going to create a web server called String server. It track of a single string that gets added to by incoming requests.
The format of request should be something look like this: 
```/add-message?s=<string>```
Here is the image of my code of this String Server:
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/StringServer%20code.png)

After we execute the program, we can then use the generated link and go to our string server. 
Here is the image of example using `Hello` after equal sign for the request:
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/StringServer-Hello%20message.png)

```Server.start(port, new Handler());``` starts the server with port number (i.e 9487) and a handler object.
When we enter the url, the `handleRequest` method is called, and the url is passed into the method as an argument.
The string array `parameters` save the string we enter in after the equal sign in the url, and elements inside
String are saved inside the string `str` and returned to the web page. That's why we can see the Hello message. 

Now we have another request is to change the string input in url to `How are you`. Here is the image of what happened:
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/StringServer-How%20are%20you%20message.png)

As you can see now, instead of `Hello`, we have both `Hello` and `How are you`. The code went through similar steps, 
but it saves the previous message request in the parameters array, so both message is being returned at once. 

Now we will went on to part 2 bugs. 
I will be using one of the bugs from lab 3 as an example, and talks about why some tests failed, and some suceed,
and how the program is fixed.

The one method that has bug that I am using is called reversed. This method will Returns a *new* array with all the 
elements of the input array in reversed order, so a array of 1, 2, 3 will be 3, 2, 1.
So I use 1, 2, 3 for one of the test to test out the method. Here's the code:
```
@Test
  public void testReversed_1() {
    int[] input1 = {1, 2, 3};
    int[] expected = {3, 2, 1};
    assertArrayEquals(expected, ArrayExamples.reversed(input1));
  }
```
And it failed. Here's the image of the failed message:
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/testReversed%20fail%20message.png)

But the program did passes this test:
```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
When testing with an empty array, it passed:
![alt text](https://github.com/Liopold35894/cse15l-lab-reports/blob/main/testReversed-empty%20array%20passed.png)

Here's the original code for this program:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
And here is the fixed code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) { 
      newArray[i] = arr[arr.length - i - 1]; 
    }
    return newArray; //should be return newArray
  }
```
So what happened is that the original code creates a `newArray`, and transfer all the elements `arr`, which basically override elements in `arr` with 0s. 
The empty array is just like creating a array without assigning elements to it, so that why the test passed.
The way I fixed this is reverse the arr and newArray inside the for loop, so the reversed elements can sucessfully assigned to newArray and return the newArray. 

Week 2's lab introduced something that I never learned before. Now I know how to launch a web server and how to play around with the url and the web page. 
Week 3's lab let me get more familier with JUnit tests. It helps me think out test cases for CSE12 PA2, and mastering the format. 
