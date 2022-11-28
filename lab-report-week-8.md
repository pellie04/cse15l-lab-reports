# Lab Report Week 8
### By Pierre Ellie


- This is the code for my grade.sh file: 


```

(comment)Create your grading script here



(comment)SCORE= 0
rm -rf student-submission
rm ListExamples.java
git clone $1 student-submission

cd student-submission
cp ListExamples.java ../
cd ..
if [ -e ListExamples.java ]
then
echo "File found"

else
echo "Wrong file or file missing. 0/5"

fi
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java 
if [ $? -eq 0 ]
then
echo ""
else 
echo "Could not compile correctly. 1/5"
exit
fi

java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore TestListExamples > testout.txt
if [ $? -eq 0 ]
then
echo "Full test passed, 5/5"
else    
cat testout.txt
echo "Some tests failed, see above for details"
exit
fi

```

- Here are some screenshots of the grader in action on a couple of different implementations  of the ListExamples java file:
![method signature](lab-5-iamges\method-sign.png)
![correct](lab-5-iamges\correct.png)
![compilererr](lab-5-iamges\compilerr.png)

- Now let's talk about the last one and trace how it would work. 

- Starting from the first lines of code, the program removes the directory called student-submission and the file ListExamples.java to make sure there isn't any collisions with the new version. These both produce no standard output and error and the return code would be 0. 

- Then, we copy over the new student-submission using git clone. This has no standard out and error as well with a return code of 0. 

- We then redirect ourselves to where ListExamples is, again no standard out and error, with return code of 0.

- Now we hit our first if statement, where we check if ListExamples.java can be found, in our case it can be, so the result would be true, leading to the echo statement for "File found", which has a return code of 0. The else echo command would not be ran because the if statement was true.

- The if statement closes and now we try to compile the java files. When compiling, we will run into out first error, creating the standard error statement detailing how there is missing semi-colon that was printed within the screenshot. The return code for this would be 1. 

- The next if statement would be false since the return code wasn't 0, which would cause the echo for the compile error message and then exiting the bash script with return code of 0. The then echo "" command would not be run since that would require the if statement to be true. 

- The next lines after 29 would not be ran because of the exit command on line 27. 