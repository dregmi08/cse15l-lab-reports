__Part 1__ : 
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
Here are two examples of `/add-message` being used:

![Image](Screen Shot 2023-01-28 at 6.28.43 PM.png)

![Image](Screen Shot 2023-01-28 at 6.31.43 PM.png)
