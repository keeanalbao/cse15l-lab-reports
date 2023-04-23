# Lab Report 2


## Part 1: StringServer
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {

    String input = "";

    public String handleRequest(URI url) {
        
        if (url.getPath().equals("/")) {
            return "This is a server";
        }

        else {
            if (url.getPath().contains("/add-message")) {
                System.out.println("Path: " + url.getPath());

                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {

                    if(input == "") {
                        input += parameters[1];
                    }
                    else {
                        input += "\n" + parameters[1];
                    }

                    return String.format("%s", input);
                }
            }

            return "404 Not Found!";
        } 
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
<img width="490" alt="4" src="https://user-images.githubusercontent.com/88350907/233804050-7250493b-a2eb-420c-9c51-9f028d28faf7.png">

For this screenshot, the program enters the first else statement in my code (since the URL path isn't just /), and then enters the `if (url.getPath().contains("/add-message"))` statement because the URL gets the current path (getPath() method from URI class) and it contains "/add-message". Next, the current path (/add-message) is printed in the terminal and a string array called parameters is created that splits the indices of the array at each `=` sign after the `?` in the URL. This `?` is retrieved by using the getQuery() method (from URI class). Next, the code enters the `if (parameters[0].equals("s"))` statement because the first index of the parameters array after the `?` is `s`. Finally, the `if(input == "")` statement is entered because the current value of the input variable is `""`, input is then updated to be the second index of the parameters array ("Hello" in this case), and then it is returned.

<img width="299" alt="2" src="https://user-images.githubusercontent.com/88350907/233803970-bcb859d6-88f6-45e2-ade0-8d0e2f08bd99.png">

In this second screenshot, all the same things are happening as the first one, but instead of entering `if(input == "")`, the code enters the corresponding else statement because the value of input is now "Hello", not `""`. In this else statement, input is updated to be a new line (`\n`) plus the second index of the parameters array (now "How are you"). Input is then returned.

<img width="365" alt="3" src="https://user-images.githubusercontent.com/88350907/233803976-b70dabf5-6d91-4bf5-b18d-816435e455b5.png">

*It is important to note that my code implements the URLHandler interface and imports the URI class, which are where all the methods used come from. Also, it's crucial to point out that it is the StringServer main method that starts the server by checking the port number after running the code.*

## Part 2: Bugs
*For this section, I decided to talk about the bug in the `reversed(int[] arr)` method in the ArrayExamples.java file. This method should return a new array with all the elements of a given input array in reverse order.*

- Failure-inducing input:
```
@Test
public void testReversed() {
    int[] input1 = { 1, 2, 3 };
    assertArrayEquals(new int[]{ 3, 2, 1 }, ArrayExamples.reversed(input1));
}
```

- Non-failure-inducing input:
```
@Test
public void testReversed() {
    int[] input1 = { 0, 0, 0 };
    assertArrayEquals(new int[]{ 0, 0, 0 }, ArrayExamples.reversed(input1));
}
```

- Symptom of the bug:

Failure-inducing input: 
<img width="664" alt="1" src="https://user-images.githubusercontent.com/88350907/233813857-15bf724c-2088-45aa-b634-b297ee1c402c.png">

Non-failure-inducing input: 
<img width="498" alt="2" src="https://user-images.githubusercontent.com/88350907/233813860-ff959a3e-72f1-4eaa-aad8-d6b50da5f9b9.png">


- Unfixed code (bugs):
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = newArray[arr.length - i - 1]; // bug
    }
    return arr; // bug
}
```
The bug here is that inside the for loop, it is setting the values of `arr` to those of `newArray` instead of setting the values of `newArray` to those of `arr`. Since `newArray` is empty, it is setting each element in `arr` to 0. So when the method returns `arr`, it returns an empty array.

- Fixed code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];

    for(int i = 0; i < arr.length; i += 1) {
        newArray[arr.length - i - 1] = arr[i]; // fixed this line
    }

    return newArray; // fixed this line
}
```
The code now sets the `arr` values to `newArray` (in reverse order of course), and returns `newArray`.


## Part 3: Something I've Learned
Something I've learned in this class from the past few weeks is actually what half this lab report is about, creating a basic web server. Prior to this class I had no idea what ports were, what the URI class and URLHandler interface were, and that you can use built-in Java libraries to create these servers. Now I have a basic understanding of how to use all these things to create my own simple server.
