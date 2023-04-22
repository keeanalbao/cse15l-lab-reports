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

<img width="299" alt="2" src="https://user-images.githubusercontent.com/88350907/233803970-bcb859d6-88f6-45e2-ade0-8d0e2f08bd99.png">

For this screenshot, the program enters the first else statement in my code (since the URL path isn't just /), and then enters the `if (url.getPath().contains("/add-message"))` statement because the URL path contains "/add-message".

<img width="365" alt="3" src="https://user-images.githubusercontent.com/88350907/233803976-b70dabf5-6d91-4bf5-b18d-816435e455b5.png">


## Part 2: Bugs


## Part 3: Something I've Learned
