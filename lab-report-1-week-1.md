# Lab Report 1
### By Pierre Ellie

##  How to use to Remote Server for your Files.

### Step 1: Setting up Visual Studio Code
1. First begin by install video studio code on your device from this [link](https://code.visualstudio.com/).
    ![vscodeinstall image](visualstudioinstall.png)
2. Once on the page, download the installer then run it.

### Step 2: Connecting Remotely
1. Now that we have VScode open, we can open the terminal to connect remotely
2. To open the terminal do Ctrl + ~ or do View > Terminal. 
3. Now, using our account, we will connect remotely by typing
- **ssh accountname@ieng6.ucsd.edu**
- *accountname will be replaced by your specific account*
4. The terminal will then prompt you to enter your password
5. Once logged in, there should be a summary of your login like shown!
[vscodeinstall image]()
### Step 3: Commands
1. Now  we can try a couple of commands to explore. Here is a few and what they do
- ls **This lists what is within the directory that you are currently in**
- ls -a **Does the same as ls but shows hidden files**
- cd *path* **This moves to another directory**    
- cat *file* **Prints the contents of the file**
- exit **logs out of the remote server**
2. Let's try a new command: scp. This commad requires a bit of set up though
3. Exit the remote server using the exit command
4. Now on your own machine create a java file called HelloRemote.java with the following code.

5. We will now move this file onto the remote server. In the terminal, write **scp HelloRemote.java accountname@ieng6.ucsd.edu:~/**
- It will ask you to enter your password for your terminal enter it to complete the move.
- If it says that the file HelloRemote.java doesn't exist, try adding the path before it to find the file OR you can use the cd and ls commands to move your terminal into the directory with HelloRemote.java


