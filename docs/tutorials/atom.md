Github and Atom Setup

 - Go to http://www.github.com and create an account by clicking the ‘Sign up‘ button on the top right.
 - Create a Repository (project): You can Read the guide or Start a project directly.
 - Copy the Clone/Download URL
 - git clone the URL (If you don’t have git installed) or see below.


         Mac:~ prmadness$ pwd
         /Users/prmadness
         Mac:~ prmadness$ which git
         /usr/bin/git
         Mac:~ prmadness$ git clone https://github.com/prmadness/new_project.git
         Cloning into 'new_project'...
         remote: Counting objects: 3, done.
         remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
         Unpacking objects: 100% (3/3), done.
         Mac:~ prmadness$  ls -ld new_project
         drwxr-xr-x  4 prmadness  staff  136 Feb  8 15:06 new_project/
         Mac:~ prmadness$ cd new_project/
         Mac:new_project prmadness$ pwd
         /Users/prmadness/new_project

 - Download the Atom editor from www.Atom.io, then install and start the application.
 - Open the Atom editor and under the File menu click on “Add Project Folder”, Then select the project folder that came down from the git clone.
 - In the Atom editor, write your python code and save the file to the repository folder using a .py (or applicable) extension.
 - If the atom-runner package is installed, you could execute the code directly from Atom pressing CTRL-R on your keyboard.
 - Go back to the command line (Terminal) and execute the following commands:

          Mac:$cd new_project/
          Mac:ucs-config prmadness$ pwd
          /Users/prmadness/new_project
          Mac:ucs-config prmadness$ git status
          On branch master
          Your branch is up-to-date with 'origin/master'.
          Untracked files:
           (use "git add ..." to include in what will be committed)

             ucs-config.py

          nothing added to commit but untracked files present (use "git add" to track)

 - Execute “git add ucs-config.py” and “git status” again

           git add ucs-config.py
           Mac:ucs-config prmadness$ git status
           On branch master
           Your branch is up-to-date with 'origin/master'.
           Changes to be committed:
             (use "git reset HEAD ..." to unstage)

               new file:   ucs-config.py

Execute “git commit -m “message” “

          Mac:ucs-config prmadness$ git commit -m "first commited file"
          [master c04a7ac] first commited file
           1 file changed, 6 insertions(+)
           create mode 100644 ucs-config.py

 - At this point, the new file is committed to the project in my laptop, but not synced up.
 - Execute “git push“

         Mac:ucs-config prmadness$ git push
         warning: push.default is unset; its implicit value has changed in
         Git 2.0 from 'matching' to 'simple'. To squelch this message
         and maintain the traditional behavior, use:

           git config --global push.default matching

         To squelch this message and adopt the new behavior now, use:

           git config --global push.default simple

         When push.default is set to 'matching', git will push local branches
         to the remote branches that already exist with the same name.

         Since Git 2.0, Git defaults to the more conservative 'simple'
         behavior, which only pushes the current branch to the corresponding
         remote branch that 'git pull' uses to update the current branch.

         See 'git help config' and search for 'push.default' for further information.
         (the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
         'current' instead of 'simple' if you sometimes use older versions of Git)

         Username for 'https://github.com': prmadness
         Password for 'https://prmadness@github.com':
         Counting objects: 3, done.
         Delta compression using up to 8 threads.
         Compressing objects: 100% (3/3), done.
         Writing objects: 100% (3/3), 346 bytes | 0 bytes/s, done.
         Total 3 (delta 0), reused 0 (delta 0)
         To https://github.com/prmadness/ucs-config.git
            fab300a..c04a7ac  master -> master

 - If this was your first time pushing a file, execute “git config –global push.default simple” to get rid of the legacy message.
 - Everyone else who wants to have the latest revision of your project must execute a “git pull” if they already cloned the project or the “git clone URL” command to download the whole project.
 - All these git commands work when you are in the repository path/folder of your laptop, use the “pwd” command to check your current path.
 - Execute git with no arguments to display the Help:

         Mac:ucs-config prmadness$ git
         usage: git [--version] [--help] [-C <path>] [-c name=value]
                    [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
                    [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
                    [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
                    <command> [<args>]

         These are common Git commands used in various situations:

         start a working area (see also: git help tutorial)
            clone      Clone a repository into a new directory
            init       Create an empty Git repository or reinitialize an existing one

         work on the current change (see also: git help everyday)
            add        Add file contents to the index
            mv         Move or rename a file, a directory, or a symlink
            reset      Reset current HEAD to the specified state
            rm         Remove files from the working tree and from the index

         examine the history and state (see also: git help revisions)
            bisect     Use binary search to find the commit that introduced a bug
            grep       Print lines matching a pattern
            log        Show commit logs
            show       Show various types of objects
            status     Show the working tree status

         grow, mark and tweak your common history
            branch     List, create, or delete branches
            checkout   Switch branches or restore working tree files
            commit     Record changes to the repository
            diff       Show changes between commits, commit and working tree, etc
            merge      Join two or more development histories together
            rebase     Reapply commits on top of another base tip
            tag        Create, list, delete or verify a tag object signed with GPG

         collaborate (see also: git help workflows)
            fetch      Download objects and refs from another repository
            pull       Fetch from and integrate with another repository or a local branch
            push       Update remote refs along with associated objects

         'git help -a' and 'git help -g' list available subcommands and some
         concept guides. See 'git help <command>' or 'git help <concept>'
         to read about a specific subcommand or concept.

 - Add the terminal-plus package to Atom to open a terminal on you current repository and execute the git commands directly from the Atom editor.
 - As an alternative to the command line add the git-plus package to use git directly from the Atom editor, after it is installed press “Command+Shift+P” to add, commit and push. To learn how to use git from atom check this video.
