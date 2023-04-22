# Lab Report 2


## Part 1
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


<img width="195" alt="1" src="https://user-images.githubusercontent.com/88350907/233803963-0fb9f831-c757-43be-acd4-30e01dc25c26.png">

<img width="299" alt="2" src="https://user-images.githubusercontent.com/88350907/233803970-bcb859d6-88f6-45e2-ade0-8d0e2f08bd99.png">

<img width="365" alt="3" src="https://user-images.githubusercontent.com/88350907/233803976-b70dabf5-6d91-4bf5-b18d-816435e455b5.png">


## Part 2


## Part 3
