## install debian
I dont believe this requiers much of an comment as we did this during class. installing debian is quite straigth forward
I did however have 1 question, why did we have to install debian in debian? was it a auto update?

## Command line basics
* I was already somewhat familiar with the command line basics from having played a little over the wire bandit during the last lesson.
* This is the reason i am not a fan of linux based systems as they aren't easy to operate, there is a lot of needles complexity involved.
* Optimally i would like a windows based system that has the ability to do everything  linux can do in CMD but also lets you just use the inteface. I am aware of linux systems that allow this, i just prefer the ease of use in windows.

a) <img width="1141" height="208" alt="image" src="https://github.com/user-attachments/assets/1c969efa-ec2e-46dc-b555-d585d0fef35f" />
b) <img width="1121" height="361" alt="image" src="https://github.com/user-attachments/assets/0d667d45-ada8-44c3-9611-8b3e3bc27511" />
c) <img width="1116" height="430" alt="image" src="https://github.com/user-attachments/assets/b256e8b0-98c9-4ba2-b0a2-f25d2f0ba33a" />

## over the wire bandit
* the first couple are pretty easy as all you gave to do is read some wierd files.
* you acces them in the following way.
```
    $ sudo ssh banditn@bandit.labs.overthewire.org -p 2220
    $ ls
    $ cat filename 
```
where n is the task name.
* there are tricks for future tasks
```
    $ ls
file name: -
    $ cat -- -
```
the -- marks the end of commands and everything afther it is a parameter
#### This next one i strugled with
The task is to open a file named --spaces in this file name--
I eventually gave up and looked online but noone elses solution worked.
the most common solution was
```
    $ cat "spaces in this filename"
```
or
```
    $ cat ./spaces\ in\ this\ filename
```
but this didn't work for me
<img width="1019" height="536" alt="image" src="https://github.com/user-attachments/assets/a2368053-a8d5-4833-a016-a1c4093bac88" />
for context the line before the 2 empty ones had a " at the end but for whatever reason it disapeared
the solution ended up being 

```
    $ cat -- "--spaces in this filename--"
```
<img width="859" height="159" alt="image" src="https://github.com/user-attachments/assets/343e398d-440b-4098-bc71-3f382a5eb925" />
### Questions
At the end i was left with only one major question, why did the commands
```
    $ cat "spaces in this filename"
    $ cat "--spaces in this filename--"
```
work for others but not for me?
For context i tried restarting the terminal so i don't have scrteenshots of all my attempts.
