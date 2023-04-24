# Lab Report 2  
  
## Part 1
  
Code for my StringServer:  
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    String stringOutput = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return this.stringOutput;
        } 
        else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    this.stringOutput += parameters[1] + "\n";
                    return this.stringOutput;
                }
                else{
                    return "invalid command";
                }
            }
            else{
                return "invalid query";
            }
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
  
Screenshots of the server working:  
  1. typing in `http://localhost:4000/add-message?s=yes`:
  ![Image](StrServerSC1.png)  
  2. typing in `http://localhost:4000/add-message?s=nope`:  
  ![Image](StrServerSC2.png)  

## Part 2:

