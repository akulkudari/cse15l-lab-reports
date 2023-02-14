# Lab Report 2
## Part 1
In Part 1 of the Lab Report I will be going through the code for my StringServer and explaining how it works. 
\
Our Handler code looks like this, I will explain what methods are called later on, but keep this as a reference. 
![StringServerCOde.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/StringServerCOde.png?raw=true)
\
This is our main method for the String Server class, it just makes sure that the port creation is handled properly. 
![StringServerStartCode.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/StringServerStartCode.png?raw=true)
The StringServer starting page looks like this. In the creation of this page, the handleRequest method is called in the Handler class, but only the first if statement is utilized as there is no query to add a message yet. 
![StringServer1.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/StringServer1.png?raw=true)
when you put "/add-message?s=<string>" in the search bar after the port name, you can add messages to the page. This calls the handleRequest method, but this time it calls the internal if statement since we pass in an argument. The url passed through is formatted in "/add-message?s=<input>", and this is checked to see if it contains "/add-message", then split from the "=" character into 2 different strings, the one before the "=", which includes "/add-message?s" and the other string which is the arguments after the "=" sign. These are stored in "parameters" which is a String type array of size 2. 
![StringServer2.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/StringServer2.png?raw=true)
Do it again and it will put the new messages on the line below the current message, calling the same method as the screenshot above.
 ![StringServer3.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/StringServer3.png?raw=true) 
  
## Part 2
  The `reverseInPlace()` method has a bug in it. \
  One failure inducing input for the method is `{1,2,3}`. we run the following code in the Tester File to check the output. \ 
  `@Test `\
  `public void testReverseInPlace() {`\
    `int[] input = {1,2,3};`\
    `ArrayExamples.reverseInPlace(input);`\
    `assertArrayEquals(new int[]{3,2,1}, input);`\
  `}`\
  this is the result: 
  ![failed Test.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/failed%20Test.png?raw=true) \
  We expect the result of calling `reverseInPlace()` on this array to give us the array {3,2,1} but instead we get {3,2,3} \
  One input that works perfectly fine for the list is `{1,1,1}` \ 
  we can test this by running the following tester code:\
  `@Test`\
  `public void testReverseInPlace2() {`\
    `int[] input = {1,1,1};`\
    `ArrayExamples.reverseInPlace(input);`\
    `assertArrayEquals(new int[]{1,1,1}, input);`\
  `}`\
  When calling `reverseInPlace()` on this list, we get the expected result of `{1,1,1}` since the list is the same backwards. \
  ![passedTest.png](https://github.com/akulkudari/cse15l-lab-reports/blob/main/passedTest.png?raw=true)\
  In order to fix the code so it works properly for both cases, we need to change the for loop.\
  We change the for loop to the following.\ 
 ` static void reverseInPlace(int[] arr) {`\
    `for (int i = 0, j = arr.length - 1; i < j; i++, j--) {`\
     ` int temp = arr[i];`\
      `arr[i] = arr[j];`\
      `arr[j] = temp;`\
  `}`\
  `}`\
And now when we run the code it will work as expected.\
![image](https://user-images.githubusercontent.com/122570367/218639758-a20fc363-d8a3-4a7f-a92c-156812ecc372.png)\
## Part 3
  One thing that I've learned in week 2 and 3's lab session is how to start a web server from your laptop, and how to create things like a simple search engine, a number incrementer, and a server that keeps track of strings. We can do this by first creating a Java file for the server functionality, and implementing a Handler class that will deal with the requests from the URL from the user. Then once we decide the functionality of the handler class, we then implement the main method by declaring how the command line argument will determine the port number, and including a Server.start method call to start the server. We can then compile the server file we built along with the Server.java file, and if it compiles correctly, we run the server file and our local server host is created. 
