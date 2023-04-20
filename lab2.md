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

## Part 2


## Part 3
