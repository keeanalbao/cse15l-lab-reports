# Lab Report 2


## Part 1
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {

    String input = "";

    public String handleRequest(URI url) {
        
        if (url.getPath().equals("/")) {
            return "This is server 4000";
        }

        else {
            if (url.getPath().contains("/add-message")) {
                System.out.println("Path: " + url.getPath());

                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {

                    input += "\n" + parameters[1];

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

<img width="359" alt="1" src="https://user-images.githubusercontent.com/88350907/233470776-6bbc839b-704c-4680-85a3-d9959be675ef.png">

<img width="419" alt="2" src="https://user-images.githubusercontent.com/88350907/233470828-e61c4309-c91a-4bbe-a501-315f86b60c75.png">


## Part 2


## Part 3
