# Lab Report Week 6
### By Pierre Ellie

### Part 1
- Me and my partner did the challenge task, but for this report I did the first prompt about changing start to base.
These were my inputs:
```
/start <enter> ce base <esc> n . n . :wq <enter>
```
- Total keys: 22

-For the first sequence up to `<enter>` it will find the instance of start like in the image shown. 
![start example](lab-7-images\start-example.png) 

- Next, the ce then typing base will take out the word start and type out the word base as it's replacement, finally exiting insert mode with `<esc>`.
![ce example](lab-7-images\ce-example.png)

- Now since going into insert mode and making the change is the exact same keys from before, we just need to press n to find the next instance and press . to do the previous step again
![next example](lab-7-images\next-example.png)

- After doing this one more time, we can type the :wq and press `<enter>` to write and exit vim.
![final example](lab-7-images\final-example.png)

### Part 2

- Making the changes on my own machine and uploading them took 46 seconds as well 1m05s for a more complicated change. 
- When I made the same steps doing it completely remotely, it took 43 seconds and 1m15s seconds for the more complicated change.
- In both cases I tried to use the same shortcuts for both instances, the noticable time usage from the first method was having to upload the files in the right place, while for doing it remotely, it was navigating the remote server as well as taking slightly longer using vim than vscode. 

- I think I would prefer the second method in most cases because many changes that are made can be done are minor and I can become faster at using vim to make said changes. On the other hand, for more large files that I have to make from scratch I'd rather have the assistance of visual studio code, even if it means some time lost. At the end of the day if I think I'm going to be spending more time actually writing the code as opposed to moving it or using it, I'd want to use a easy compiler like vscode, but minor changes and quickly going in and out of running the code itself, remote is more convenient for me. 