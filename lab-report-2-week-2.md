# Lab Report 2
### By Pierre Ellie

##  Part 1: Lab 2

- Here is code for my Search Engine I made in Lab 2. 
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> messages = new ArrayList<String>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Welcome to the String page!");
        } else if (url.getPath().contains("/search")) {
            String[] parameters1 = url.getQuery().split("=");
            if (parameters1[0].equals("s")) {
                ArrayList<String> results = new ArrayList<String>();
                for (int i = 0; i < messages.size(); i++) { 
                    if(messages.get(i).contains(parameters1[1])){
                        System.out.println(messages.get(i));
                        results.add(messages.get(i));
                        
                        
                    }
                  }
                  return String.format("%s ",results);
                
            }
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters2 = url.getQuery().split("=");
                if (parameters2[0].equals("s")) {
                    System.out.println(parameters2[1]);
                    messages.add(parameters2[1]);
                    System.out.println(String.format("This list now contain %s", messages));
                    return String.format("String added! We now know %s", parameters2[1]);
                }
            }
            return "404 Not Found!";
        }
        return "404 Not Found!";
    }
}

class SearchEngine {
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
- It can still be optimize but it current does work, here are a couple of examples of pages ran.

![image1part1 image](lab-2-images\part1-image1.png)
- When running this command on the site, the handleRequest method is ran, it then runs through the two if statements, returning false on both, then gets true on the if statmment for if add is included. It splits up the query, finding the s key then the terms after the equals sign, in this case "apple". "apple" gets added to Arraylist of the added strings, then returns the message about the string being added with the returned string. 

![image3part1 image](lab-2-images\part1-image3.png)
- This url has the term search, which means that when running the handleRequest, it will return true on the if statement looking for search. This causes it then to split the query for the searched term, then run a for loop checking each term in the array list with the .contains command to see if it contained the search term. It then returns a new List with the terms that returned true. 

![image2part1 image](lab-2-images\part1-image2.png)
- This url has a type within it. "seh" is not a command within the java file, so it doesn't pass any of the if checks for either add or search, so it would return the error message. Similarly, if there is no server port, it would return another error message. 

##  Part 2: Lab 3