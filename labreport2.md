__Part 1__ : Looking up your CSE 15L account 
---

This is an image of my `StringServer.java` file
![Image](Screen Shot 2023-01-28 at 6.19.25 PM.png)

Here is the code written out in a code block:
```
import java.io.IOException;
import java.net.URI;


class Handler implements URLHandler{
    String webPage = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            webPage += ("\n " + parameters[1]);
            return webPage;
        }
        else {
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

