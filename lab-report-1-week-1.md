# Lab Report 1
### By Pierre Ellie

##  How to use to Remote Server for your Files.

### Step 1: Setting up Visual Studio Code

1. First begin by install visual studio code on your device from this [link](https://code.visualstudio.com/).
    ![vscodeinstall image](visualstudioinstall.png)
2. Once on the page, download the installer then run it.
<<<<<<< HEAD
- Due to complications with password changing, the images are from the active directory personal I had used.

- Due to complications with password changing, the images are from the active directory personal I had used. 


### Step 2: Connecting Remotely

1. Now that we have VScode open, we can open the terminal to connect remotely.
2. To open the terminal do Ctrl + ~ or do View > Terminal. 
3. Now, using our account, we will connect remotely by typing:
- **ssh accountname@ieng6.ucsd.edu**
- *accountname will be replaced by your specific account*
- To find the account name, go to this [link](https://sdacs.ucsd.edu/~icc/index.php). When at the site, you can login with your username and PID to find your account name. 

4. The terminal will then prompt you to enter your password.
5. Once logged in, there should be a summary of your login like shown.
![loginresults image](lab1loginresult.png)

### Step 3: Commands

1. Now  we can try a couple of commands to explore. Here is a few and what they do:
- ls **This lists what is within the directory that you are currently in**
- ls -a **Does the same as ls but shows hidden files**
- cd *path* **This moves to another directory**    
- cat *file* **Prints the contents of the file**
- exit **logs out of the remote server**
![code example image](codeexample.png)
2. Let's try a new command: scp. This commad requires a bit of set up though.
3. Exit the remote server using the exit command.

### Step 4: Moving files

1. Now on your own machine create a java file called HelloRemote.java with the following code.
```
class HelloRemote {
    public static void main(String[] args){
        System.out.println("Hello server!");
        System.out.println("Here is some of information about this system: ");
        System.out.println("os.name!");
        System.out.println("user.name");
        System.out.println("user.home");
        System.out.println("user.dir");
    }
}
```

2. We will now move this file onto the remote server. In the terminal, write **scp HelloRemote.java accountname@ieng6.ucsd.edu:~/**
- It will ask you to enter your password for your terminal enter it to complete the move.
- If it says that the file HelloRemote.java doesn't exist, try adding the path before it to find the file OR you can use the cd and ls commands to move your terminal into the directory with HelloRemote.java
3. Now that the file is on the server, we can reconnect to it to run the file using the ssh command from before.
4. Compile and run the file by typing **javac HelloRemote.java** then **java HelloRemote** and see the printed results
![HelloRemoteResults image](helloremoteresults.png)
- We can also see the code of the file with the **cat** command

### Step 5: Setting up an SSH key

1. Notice how we ned to use a password for every movement of files and every time we try logining into the remote server. We can make this process faster by using an SSH key. 
2. On your own computer, type the command **ssh-keygen**
3. When prompted with file and passphrase, just press enter to have defaults.
- This would be the results
![sshkeyresults image](sshkeyresults.png)
4. This results in a couple files being made as well, if you type **ls -a** you should be able to see them with the names **id_rsa id_rsa.pub**.
5. Now we will create a directory on the server by reconnecting to it and typing **mkdir .ssh**. Then logout of the server using **exit**
6. Now copy the key over using the command **scp /Users/you/.ssh/id_rsa.pub youraccount@ieng6.ucsd.edu:~/.ssh/authorized**.
- Now you might be able to connect to the remote server without a password. This did not work for me though, it still asks for a password but I think this issue might have to do with using my active directory as opposed to the class account.
 ![sshkeyfail image](sshkeyfail.png)
 - It says my Macbook is in the file authorized, yet I still need to type the password to log into it.

### Optimizing

- Now we can think about how to move things more quickly, obviously my key did not work so I had to do this mostly in theory but we can think about ways to make things quick when working in our terminal.
- I personally had to use a compiler to make my Java file, but if there was a way to edit the file within the terminal, similar to using the cat command and rewriting some portions, it may make the process quicker as one does not need to leave a re-enter the terminal many times to write their file. 
-Assuming this was possible and the key worked, I could quickly make a change within the terminal to my java file or even multiple, then scp them all into the server without my a password using only 1 command.  
-When working thinking about moving mutliple files, we can just extend the command with spaces. In this image I did that by adding the text1-copy.txt as well text1 in the same command. Although there was a file that didn't exist, it was still able to move the other 2 files.
![sshkeyfail image](optimaltest.png)

- With this knowledge, we could move a large amount of files, even if some of them don't exist. For example, if we wanted to move information about 10 people, but only 7 have information, as long as the file naming is correct we could move those 7 files when trying to move all 10 without many issues. 
### Congrats

 - You have worked with the remote server, hopefully no issues came up like for me and now you can move and access the server freely for future works!

