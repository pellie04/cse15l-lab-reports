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
### Array Methods: averageWithoutLowest
- I wrote the following tests for this method: 
```
@Test  
public void testAverageLowestEmpty(){    
    double[] input1 = { 3 };    
    assertEquals(0.0, ArrayExamples.averageWithoutLowest(input1), 0);  
    }  
    @Test  
    public void testAverageLowest(){    
        double[] input1 = { 3, 3, 3, 4, 4, 4, 10 };    assertEquals(4.66666, ArrayExamples.averageWithoutLowest(input1), 0.01);  
        }
``` 
- The resons I wrote two tests was because I wanted to check for two different symptoms: 1. It did not return 0 if there was a single input like it was supposed to and 2. if the average was actual calculated correctly. 
- When running these tests I got the following results: 
![image2part2 image](lab-2-images\part2-image2.png)



- So the symptom here was number 2, which means that there is something wrong within the method when trying to calculate the average of the list without the lowest term. In this case, the average was way too low, so I guessed there was something wrong with removing the lowest number from the list. 
- When looking at how the bug may have caused this symptom, I reversed the math that the method did, by multiplying 3.66666 times 6, I got 22. So when removing every 3, but still counting for 6 values, there was a incorrect average. (4+4+4+10)/6 . This meant that 3 was being removed too many times. 
- When looking at the code, I noticed that the method kept track of the lowest number by storing it inside of a double variable. I found this unreliable because of an instance like the test where there multiple of that lowest number. So when changing the code, I added another variable that would keep track of the lowest index, and when checking which number to remove, it did it based on index not value. 
![image2part3 image](lab-2-images\part2-image3.png)
- When I ran the tests again, they passed: 
![image2part4 image](lab-2-images\part2-image4.png)



### List Methods 
```
@Test    
public void testFilter(){        
    List<String> input1 = new ArrayList<>();        
    input1.add("cool");        
    input1.add("color");        
    input1.add("hello");              
    assertArrayEquals(input1.toArray() , ListExamples.filter(input1, new myChecker()).toArray());    }
```
- This is a test for the filter method in the ListExamples class. This class is supposed to check if input is string and return the list changed to having only strings. This test takes 3 strings, "cool" "color" and "hello" and asks to filter it. The test should pass if nothing changes with the list.
- This test failed though, with this report:
![image1part2 image](lab-2-images\part2-image1.png)
- This meant that there was an error with the returned List of strings, which only had one value in it, not the 3 that were needed. Reading the code I found the bug on line 15 where there was the statement:
```
result.add(0, s);
```
- This meant that it would only change the value at index 0 in the results list. This would mean that there would only be 1 value within the list, which would cause the symptom of the second item never being found because it never tried to add anything there in the first place. 
- To fix this, I created a index variable, changed the add to the index and increased index after each add. This resulted in this code: 
```
int index = 0;    
for(String s: list) {      
    if(sc.checkString(s)) {        
        result.add(index, s);        
        index++;      
        }    
    }
```
- After making these changes, the test passed! The resulting list matched the expected one and the code ran smoothly. 