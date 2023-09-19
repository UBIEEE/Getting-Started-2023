# Getting Started with IEEE 2023

## Introduction

Welcome the University at Buffalo IEEE Micromouse! This repository is a collection of resources to help you get started with the Micromouse project. If you have any questions, please reach out to [Eric Butcher](mailto:ericbutc@buffalo.edu). Please first got to the software section and download all the required software there. After you have downloaded the necessary software, please continue to the practicing git section and complete the steps laid out there. 

## Software

### Git

Git is a version control system that allows you to track changes to text files. It is a very powerful tool that is used in industry and is a great skill to have. We will be using git to track changes to our code and to share code with each other.

You can install git on Debian based Linux by typing the following command into a terminal:

```bash
sudo apt install git
```

You can install git on Windows by downloading the installer from [here](https://git-scm.com/download/win).

### Visual Studio Code

Visual Studio Code is a powerful and relatively lightweight text editor. It has many features that make it a great choice for programming. We will be using Visual Studio Code to write anything not in Java. VSCode also has the ability to take care of GitHub credentials so that you can access remote GitHub repositories without needing to create an SSH key. You can download Visual Studio Code from [here](https://code.visualstudio.com/download).

### GitHub 

Please go to [GitHub](https://github.com/) and create an account. After you have created an account, please text your GitHub username __exactly__ in the Micromouse discord channel. This will allow us to add you to IEEE's GitHub organization. All repositories for the Micromouse project will be hosted on the [UB IEEE GitHub organization](https://github.com/). 

Each IEEE project will have its own set of teams inside of the GitHub organization, and each team will have access to the repositories for that project. For example, the Micromouse project will have a team called `Micromouse 2023`, and all members of the `Micromouse 2023` team will have access to the Micromouse repositories. 

### IntelliJ IDEA

IntelliJ Idea is a powerful IDE for Java development. It has many features that make it a great choice for developing programs in Java. We will be using IntelliJ Idea to write all of our Java code. You can download IntelliJ Idea from [here](https://www.jetbrains.com/idea/download/). IntelliJ is nice because it will also take care of your GitHub credentials for you, meaning that you won't have to create a SSH key. 

If you are planning on using or working on the simulator at all, you will working in IntelliJ as the simulator is a Java program. 

## Practicing Git

1. Double check that you have git installed. You can do this by typing `git --version` into a terminal. If you get an error, please go back to the software section and install git.

2. Locate or create a directory (a folder) in which you would like to keep you programming projects for IEEE. For example, I keep a directory called `Projects` in my home directory for all of my programming projects. My `Projects` directory contains all of the directories of my individual projects. What you call this directory and where you place it are not that important as long as it is easily accessible.

3. Open VSCode. Click on the `Explorer` icon and select `Open Folder`. Navigate to the directory you just created and click `Open`. You should now have a workspace open in VScode within that folder. If you click on the `Explorer` menu you should see a directory structure of everything inside of the folder you opened, unless the folder you opened was empty. 

4. Click on the `Terminal` menu and select `New Terminal`. This will open a terminal window at the bottom of the VSCode window. The last directory in the terminal prompt should be the directory you opened in VSCode. If it is not, please go back and open the correct folder. 

5. Next, we will `clone` this repository that you are currently reading from. Cloning a repository means that we are downloading a copy of the repository to our local machine. To clone this repository, type the following command into the terminal:

    ```
    git clone https://github.com/UBIEEE/Getting-Started-2023.git
    ```

    You may be prompted to enter your GitHub username and password. If you are, please do so. 

    If you click on the refresh icon on your folder in the `Explorer` you should now see a folder called `Getting-Started-2023`. This is the repository you just cloned. 

6. Generally, we want to set out workspace in VSCode so that our topmost directory in the `Explorer` is the project directory itself. Click on the `File` menu and select `Close Folder`. This will close the folder you have opened in VSCode. Next, click on the `File` menu again and select `Open Folder`. Navigate to the folder of the repository we just cloned and open it up. You should now see the repository `Getting-Started-2023` as the topmost folder in `Explorer`.

7. You will now create a new git `branch`. Branching in git is a way to keep different edits to source files in separate places so that people do not have to constantly be writing all of their different changes onto the same files directly. Generally, anytime you are working on a new feature or bug fix, you will want to create a new branch. To create a new branch, type the following command into the terminal:

    ```
    git branch <branch-name>
    ```
    with `<branch-name>` being the name of the branch you want to create. Please title your branch in the following format: `firstname_lastname`. Notice that we used an underscore in the branch name. You should generally not include whitespace in branch names. 

8. In the folder you will find the code for the README.md you are reading off of right now! You will also find a subdirectory called `persons`. Create a new .txt file in the `persons` directory named by the convention `Firstname_Lastname.txt`. 

9. In the .txt file you just created, type your full name into the first line, and save. Then go back to your terminal and type the following command:
    ```
    git add Firstname_Lastname.txt
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

12. Now, go back to the GitHub page for this repository. You should see a notification that you have created a new branch. Click on the `Compare & pull request` button. This will take you to a page where you can create a pull request. A pull request is a request to merge your branch into the `main` branch. The `main` branch is the default branch for a repository. All repositories for Micromouse will have `branch protection rules` in place. In this context, a branch protection rule prevents someone from forcefully pushing code to the main branch without first undergoing a `pull request`, which is a GitHub feature that allows other members on the project to review your code before it becomes apart of the `main` branch. The `main` branch should only ever contain code that is working. Feature development and bug fixes should always be done in separate branches, and them merged in. You should (almost) __NEVER__ commit or push directly to the main branch unless you are working on a project by yourself. 
