## Git Basics for LTI

1. Verify the git installation

    ```cmd
    $ git --help
    ```

2.  Installing GIT (Incase above command fails)
    For Windows:
    Visiting git-scm.com/download/win
    Use downloaded installer.

    For Linux:
    $ sudo yum install -y git
    or
    $ sudo apt install -y git

    For MacOS:
    $ brew install git

3.  One time setup (Mandatory) 
    The username and email would be used in ALL repositories in current system.

    ```cmd
    $ git config --global user.name "Mahendra Shinde"
    $ git config --global user.email "MahendraShinde@synergetics-india.com"
    ```
4.  Create your FIRST git repository!
    ```cmd
    $ mkdir git-basics-lti
    $ cd git-basics-lti
    $ git init .
    $ echo "Hello World" > Readme.md
    $ git status
    ```

5.  The last command would display message as 
    ```cmd
    On branch master

    No commits yet
    Untracked files:
    (use "git add <file>..." to include in what will be committed)
            Readme.md

    nothing added to commit but untracked files present (use "git add" to track)
    ```

6.  Stage the file (Inform GIT, you want this file tobe version controlled)
    ```cmd
    $ git add Readme.md
    $ git status
    ```

7.  The last command should display message as 
    ```cmd
    On branch master

    No commits yet

    Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
            new file:   Readme.md
    ```

8.  Commit the changes to local repository!
    ```cmd
    $ git commit -m "First Commit"
    ```

9.  Output from last command should be:
    ```cmd
    [master (root-commit) df2a9d1] First commit
    1 file changed, 29 insertions(+)
    create mode 100644 Readme.md
    ```

10. Lets create a remote repository on github. (Please signup on github.com)
    Create a new `PUBLIC` repository.
    DO NOT CREATE README file or LICENCE 
    NOTE: Your GITHUB username (email) MUST MATCH with "user.email" configuration you have added in local git installation.

11. Copy the repository URL (of newly created github repository) and add new remote "origin" to local repository.

    ```cmd
    $ git remote add origin <<PASTE-URL-REMOTE-REPO>>
    $ git push -u origin master
    ```

12. Refresh the GitHub repository page in web browser!
