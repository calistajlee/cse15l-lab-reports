# Week 6 Lab Report

## Streamlining ssh Configuration
**Show your .ssh/config file, and how you edited it (with VScode, another program, etc)**
![.ssh/config file](streamliningssh1.png)
I edited my `.ssh/config` file using Notepad.

**Show the `ssh` command logging you into your account using just the alias you chose.**
![ssh command](streamliningssh2.png) 
I logged into my account using `ssh ieng6calista`, which is my alias that I chose.

**Show an `scp` command copying a file to your account using just the alias you chose.**
![scp command](streamliningssh3.png)
I used `scp MarkdownParseTest.java ieng6calista:~` to copy MarkdownParseTest.java from my client to the server

---

## Setup Github Access from ieng6
**Show where the public key you made is stored on Github and in your user account (screenshot).**
![public key stored on Github and in user account]()

**Show where the private key you made is stored on your user account (but not its contents) as a screenshot.**
![private key location]() 

**Show running `git` commands to commit and push a change to Github while logged into your ieng6 account.**
![running git commands to commit and push into ieng6]()

**Show a link for the resulting commit.**
[link to resulting commit]()

---

## Copy whole directories with `scp -r`
**Show copying your whole markdown-parse directory to your ieng6 account.**
![copying whole markdown-parse directory to ieng6 account1](copywholedir1.png)
![copying whole markdown-parse directory to ieng6 account1.1](copywholedir1.1.png)
![copying whole markdown-parse directory to ieng6 account1.2](copywholedir1.2.png)
I used the command `scp -r . ieng6calista:~/group-clone-markdown-parser` to copy the whole directory to my ieng6 account.

**Show logging into your ieng6 account after doing this and compiling and running the tests for your repository.**
![logging into ieng6 account and compiling](copywholedir2.png) 
In this picture, I log into my ieng6 account and compile the tests for my repository by compiling with command `javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java` and running the program with `java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest`.

**Show (like in the last step of the first lab) combining `scp`, `;`, and `ssh` to copy the whole directory and run the tests in one line.**
![running tests in one line]()

