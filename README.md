# Getting Started with IEEE 2023

## Introduction

Welcome the University at Buffalo IEEE Micromouse! This repository is a quick way to help you get started with the Micromouse project. If you have any questions, please reach out to [Eric Butcher](mailto:ericbutc@buffalo.edu). Please first got to the software section and download all the required software there. After you have downloaded the necessary software, please continue to the practicing git section and complete the steps laid out there. 

## Software

### Git

Git is a version control system that allows you to track changes to text files. It is a very powerful tool that is used in industry and is a great skill to have. We will be using git to track changes to our code and to share code with each other.

You can install git on Debian based Linux by typing the following command into a terminal:
```bash
sudo apt install git
```

You can install git on macOS by following the instructions [here](https://git-scm.com/download/mac). It is recommended to use homebrew or Apple's XCode CLI tools to install git on macOS.

You can install git on Windows by downloading the installer from [here](https://git-scm.com/download/win). You can also install git on Windows using the following command in a powershell terminal:
```powershell
 winget install --id Git.Git -e --source winget 
 ```

### Visual Studio Code

Visual Studio Code is a powerful and relatively lightweight text editor. It has many features that make it a great choice for programming. We will be using Visual Studio Code to write anything not in Java. VSCode also has the ability to take care of GitHub credentials so that you can access remote GitHub repositories without needing to create an SSH key. You can download Visual Studio Code from [here](https://code.visualstudio.com/download). 

### GitHub 

Please go to [GitHub](https://github.com/) and create an account. After you have created an account, please text your GitHub username __exactly__ in the Micromouse discord channel. This will allow us to add you to IEEE's GitHub organization. All repositories for the Micromouse project will be hosted on the [UB IEEE GitHub organization](https://github.com/). 

Each IEEE project will have its own set of teams inside of the GitHub organization, and each team will have access to the repositories for that project. For example, the Micromouse project will have a team called `Micromouse 2023`, and all members of the `Micromouse 2023` team will have access to the Micromouse repositories. 

### IntelliJ IDEA

IntelliJ Idea is a powerful IDE for Java development. It has many features that make it a great choice for developing programs in Java. We will be using IntelliJ Idea to write all of our Java code. You can download IntelliJ Idea from [here](https://www.jetbrains.com/idea/download/). IntelliJ is nice because it will also take care of your GitHub credentials for you, meaning that you won't have to create a SSH key. IntelliJ has a free community edition that is more than enough for our purposes. You may also apply for a free student license to use the Ultimate edition, but this is not necessary.

If you are planning on using or working on the simulator at all, you will working in IntelliJ as the simulator is a Java program. 

### Python

Python is a powerful programming language that is used in many different applications. Python is a powerful tool that we will use to do data analysis. Python is also a dependency forYou can download Python from [here](https://www.python.org/downloads/). Make sure to download Python 3.9.6 or later.


### gcc

gcc is a compiler for the C programming language. It is important to make sure that you have gcc as it will be a dependency for use in testing and c code written for micro-controllers.

Open a terminal and type the following command:

```
gcc --version
```
to see if you have gcc installed. 

If you do not have gcc installed, you can install it on Debian based Linux by typing the following command into a terminal:

```bash
sudo apt install build-essential
```

You can install gcc on macOS via xcode or homebrew. 
For homebrew, type the following command into a terminal:

```zsh
brew install gcc
```
For xcode, type the following command:
    
```zsh
xcode-select --install
```

Installing gcc through MinGW on Windows:
1. Download the MinGW Installer:
        https://sourceforge.net/project/showfiles.php?group_id=2435&package_id=240780
2. Select Save File when prompted.
3. Open the downloaded exe.
4. Click Yes when Windows asks if you want to allow it.
5. Click Next > on the Welcome screen.
6. Select Download and Install and click Next >
7. Read the License Agreement and click I agree
8. Select Current to install the current MinGW package and click Next >
9. Check the MinGW base tools and g++ compiler click Next
10. Destination Folder should be C:\MinGW
11. Click Next >
12. Leave the default folder and click Install
13. When Installation is complete, click Next >
14. Click Finish



## Practicing Git

1. Double check that you have git installed. You can do this by typing `git --version` into a terminal. If you get an error, please go back to the software section and install git.

2. Locate or create a directory (a folder) in which you would like to keep you programming projects for IEEE. For example, I keep a directory called `Projects` in my home directory for all of my programming projects. My `Projects` directory contains all of the directories of my individual projects. What you call this directory and where you place it are not that important as long as it is easily accessible, with two exceptions: the folder should not be inside a preexisting git repository, and the folder should not be inside a cloud storage folder such as Google Drive, OneDrive, or iCloud. 
    > Technically it is possible to have a git repository inside of another git repository, but this is generally not a good idea. Nested git repositories can cause issues with tracking changes to files, and are an advanced topic. __Do not__ create a git repository inside of another git repository. If you do, we will not help you. 

3. Open VSCode. Click on the `Explorer` icon and select `Open Folder`. Navigate to the directory you just created and click `Open`. You should now have a workspace open in VScode within that folder. If you click on the `Explorer` menu you should see a directory structure of everything inside of the folder you opened, unless the folder you opened was empty. 

4. Click on the `Terminal` menu and select `New Terminal`. This will open a terminal window at the bottom of the VSCode window. The last directory in the terminal prompt should be the directory you opened in VSCode. If it is not, please go back and open the correct folder. 

5. Next, we will `clone` this repository that you are currently reading from. Cloning a repository means that we are downloading a copy of the repository to our local machine. To clone this repository, type the following command into the terminal:

    ```
    git clone https://github.com/UBIEEE/Getting-Started-2023.git
    ```

    You may be prompted to enter your GitHub username and password. If you are, please do so. 

    If you click on the refresh icon on your folder in the `Explorer` you should now see a folder called `Getting-Started-2023`. This is the repository you just cloned. 

6. Generally, we want to set all workspaces in VSCode so that our topmost directory in the `Explorer` is the project directory itself. Click on the `File` menu and select `Close Folder`. This will close the folder you have opened in VSCode. Next, click on the `File` menu again and select `Open Folder`. Navigate to the folder of the repository we just cloned and open it up. You should now see the repository `Getting-Started-2023` as the topmost folder in `Explorer`.

7. You will now create a new git `branch`. Branching in git is a way to keep different edits to source files in separate places so that people do not have to constantly be writing all of their different changes onto the same files directly. Generally, anytime you are working on a new feature or bug fix, you will want to create a new branch. To create a new branch, type the following command into the terminal:

    ```
    git branch <branch-name>
    ```
    with `<branch-name>` being the name of the branch you want to create. Please title your branch in the following format: `firstname_lastname`. Notice that we used an underscore in the branch name. You should generally not include whitespace in branch names. 

    Next we will `checkout`, or switch to the branch we just created. 
    Type the following command into the terminal:
    ```
    git checkout <branch-name>
    ```

8. In the folder you will find the code for the README.md you are reading off of right now! You will also find a subdirectory called `persons`. Create a new .txt file in the `persons` directory named by the convention `Firstname_Lastname.txt`. 

9. In the .txt file you just created, type your full name into the first line, you major in the second, and anything else you would like to mention in the third (be nice!). Save the file. Then go back to your terminal and type the following command:
    ```
    git add .\persons\Firstname_Lastname.txt
    (Windows)

    or 

    git add ./persons/Firstname_Lastname.txt
    (UNIX)
    ```
    with the Firstname and Lastname being your first and last name. This command will add the file you just created to the list of files that git is tracking. 

    To check this, you can type the following command into the terminal:
    ```
    git status
    ```
    which should show that file as `staged`. 

10. Next, we will `commit` the file. Committing a file means that we are saving the file to the git repository. To commit the file, type the following command into the terminal:
    ```
    git commit -m "A message about this commit"
    ```

    with `A message about this commit` being a message about the commit. This message should be short and descriptive. The `-m` flag tells git that the next thing we type will be the commit message. If you did not include the `-m` flag, git would open up a text editor for you to type the commit message in. Oftentimes the default text editor will be a CLI text editor such as `vim` or `nano`. If you are not familiar with these editors, it is best to use the `-m` flag.

    > If this is the first time committing with git on your machine, you may be prompted to enter your name and email. If you are, please do so. Make sure to use the same email that you used to create your GitHub account.

    You can use `git status` again to see that the file is now added to the commit.

11. Next, we will `push` the commit to the remote repository. Pushing a commit means that we are uploading the commit to the remote repository. To push the commit, type the following command into the terminal:
    ```
    git push
    ```

    At this point you will likely face an error message. Do not worry! Git is just telling us that we need to specify the name of the `remote branch` that we must add our commit to. Git will most likely prompt you to type a command such as the following, which you should type into the terminal:
    ```
    git push --set-upstream origin <branch-name>
    ```

    This will create a branch on the remote repository with the same name as the branch you created locally.

12. Now, go back to the GitHub page for this repository. You should see a notification that you have created a new branch. Click on the `Compare & pull request` button. This will take you to a page where you can create a pull request. A pull request is a request to merge your branch into the `main` branch. The `main` branch is the default branch for a repository. All repositories for Micromouse will have branch protection rules in place. In this context, a branch protection rule prevents someone from forcefully pushing code to the main branch without first undergoing a pull request, which is a GitHub feature that allows other members on the project to review your code before it becomes apart of the `main` branch. The `main` branch should only ever contain code that is working. Feature development and bug fixes should always be done in separate branches, and them merged in. You should (almost) __NEVER__ commit or push directly to the main branch unless you are working on a project by yourself. 


## Using PlatformIO

PlatformIO is a powerful tool that allows us to write code for micro-controllers in a variety of languages. PlatformIO is a plugin for Visual Studio Code. You can install PlatformIO by clicking on the `Extensions` icon in the left sidebar of VSCode and searching for PlatformIO.

This is one option for writing code for micro-controllers. You may also use the Arduino VSCode extension if you wish. 

1. Install the PlatformIO extension for VSCode. Do this by going into the left sidebar of VSCode and clicking on the `Extensions` icon. Search for PlatformIO and click `Install`. PlatformIO has Python 3.6+ has a dependency, so make sure you have first installed python. 

2. Next, we will create a new PlatformIO project. Click on the `PlatformIO` icon in the left sidebar of VSCode. Click on `New Project`. Select `Arduino` as the framework. Select `Arduino Uno` as the board. Select the directory you want to create the project in and create it there. 

3. You should now see a new directory in the `Explorer` called `src`. This is where we will put the main file that will run in our program. Try copying and pasting this basic blink program into the main .cpp file that was created in the src directory. 

    ```
    #include <Arduino.h>

    void setup() {
    // initialize digital pin LED_BUILTIN as an output.
    pinMode(LED_BUILTIN, OUTPUT);
    }

    // the loop function runs over and over again forever
    void loop() {
    digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
    delay(1000);                      // wait for a second
    digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
    delay(1000);                      // wait for a second
    }
    ```

4. Try uploading this to an Arduino Uno Board. You should see an LED blinking on and off.

5. Next, go into the lib folder and create a new folder inside called `metric`. Inside of this folder create two files, one called `metric.c` and another called `metric.h`. Copy-and-paste the code below into `metric.c`:
    ```
    #include "metric.h"

    int time_to_milliseconds(int time) {
        int retVal =  time * 1000;
        if (retVal < 0) {
            return -1;
        }
        return retVal;
    }
    ```

    and this code into metric.h:
    ```
    #ifndef _CALCULATOR_H_
    #define _CALCULATOR_H_

    #ifdef __cplusplus
    extern "C"
    {
    #endif

    int time_to_milliseconds(int time);


    #ifdef __cplusplus
    }
    #endif

    #endif // _CALCULATOR_H_
    ```

6. In the previous step, we created a library, which is a collection of code that we can use in our program. We can use this library by including it in our main program. To do this, we will add the following line to the top of our main program:
    ```
    #include <metric.h>
    ```

7. Next, try changing the 1000 in the delay function to a call to the `time_to_milliseconds` function. Experiment with different delays. Upload the program to the board. You should see that the program still works.

8. Try playing around on your own. In the future we will be discussing how to do testing in PlatformIO. 


## Using the Simulator

The simulator is a Java program that simulates a micromouse maze. The simulator is a great tool for testing algorithms and for testing the mouse itself. Currently, the simulator supports maze generation with two different algorithms and maze solving with two different algorithms. 

1. Locate the simulator in the UBIEEE GitHub organization. Clone the repository to your local machine.You can do this by going to IntelliJ and selected `Get from VCS` option. You can copy and paste the GitHub url into the `URL` field. You may have to sign into GitHub.

2. Open up the README.md and read through it so that you understand the basic structure. 

3. Open up the project in IntelliJ. You can do this by clicking on the `File` menu and selecting `Open`. Navigate to the directory you cloned the repository to and open it.

4. Run the simulator by generating and solving mazes observe how it functions. 

5. Check out the page [here](https://github.com/orgs/UBIEEE/projects/2). This will take you to the project page. We will discuss the fututre development of the simulator. 