
C:\Users\HAMI>cd C:\webproject

C:\webproject>git init
Initialized empty Git repository in C:/webproject/.git/

C:\webproject>git add script.js style.css index.html


C:\webproject>git commit -m " avalin commit ba file haye js,css.html"
[master (root-commit) e26a4b3]  avalin commit ba file haye js,css.html
 3 files changed, 17 insertions(+)
 create mode 100644 index.html
 create mode 100644 script.js
 create mode 100644 style.css

C:\webproject>git branch feature/update-title

C:\webproject>git branch
  feature/update-title
* master

C:\webproject>git checkout feature/update-title
Switched to branch 'feature/update-title'


C:\webproject>git add index.html

C:\webproject>git commit -m"onvan dar index.html beroz resani shod"
[feature/update-title d77153a] onvan dar index.html beroz resani shod
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\webproject>git checkout master
Switched to branch 'master'

C:\webproject>git merge feature/update-title
Updating e26a4b3..d77153a
Fast-forward
 index.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\webproject>git show
commit d77153a8afe5eb9d9888a2851035e2a9b7eb1fde (HEAD -> master, feature/update-title)
Author: imdorsww <shiravanifard@gmail.com>
Date:   Wed Jan 15 19:03:09 2025 +0330

    onvan dar index.html beroz resani shod

diff --git a/index.html b/index.html
index 116677b..d5a6ba8 100644
--- a/index.html
+++ b/index.html
@@ -1,7 +1,7 @@
 <!DOCTYPE html>
 <html>
 <head>
-<title> پروژه وب من  </title>
+<title>پروژه وب من بروزرسانی شد   </title>
 <link rel="stylesheet" href="style.css">
 </head>
 <body>

C:\webproject>git branch -d feature/update-title
Deleted branch feature/update-title (was d77153a).

C:\webproject>git branch feature/conflict-example

C:\webproject>git checkout feature/conflict-example
Switched to branch 'feature/conflict-example'

C:\webproject> git add index.html

C:\webproject>git commit -m"taghit dar h1 baraye ijad conflict"
[feature/conflict-example a2cee73] taghit dar h1 baraye ijad conflict
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\webproject>git show
commit a2cee7331b3c9bdb411bf003033f05eb6584b200 (HEAD -> feature/conflict-example)
Author: imdorsww <shiravanifard@gmail.com>
Date:   Wed Jan 15 19:15:46 2025 +0330

    taghit dar h1 baraye ijad conflict

diff --git a/index.html b/index.html
index d5a6ba8..ad7d68b 100644
--- a/index.html
+++ b/index.html
@@ -5,7 +5,7 @@
 <link rel="stylesheet" href="style.css">
 </head>
 <body>
-<h1> به پروژه وب من خوش آمدید</h1>
+<h1> این یک تغییر برای ایجاد conflict است</h1>
 <script src="script.js"></script>
 </body>
 </html>
\ No newline at end of file

C:\webproject>git checkout master
Switched to branch 'master'

C:\webproject>git add index.html

C:\webproject>git commit -m"taghit dar h1 main baraye ijad conflict"
[master e9d3670] taghit dar h1 main baraye ijad conflict
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\webproject>git merge feature/conflict-example
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

C:\webproject>git add index.html

C:\webproject>git commit-m" conflict raf shod"
git: 'commit-m conflict raf shod' is not a git command. See 'git --help'.


C:\webproject>git commit -m " cnflict hal shod"
[master ee525c3]  cnflict hal shod

C:\webproject>git branch
  feature/conflict-example
* master

C:\webproject>git add script.js

C:\webproject>git commit -m "afzodan hoshdar eshtebah be script.js"
[master 1e4e48e] afzodan hoshdar eshtebah be script.js
 1 file changed, 2 insertions(+), 1 deletion(-)


C:\webproject>git show f1e5d6405cf88e3dbab79f1ae3078762f1246df1
commit f1e5d6405cf88e3dbab79f1ae3078762f1246df1 (HEAD -> master)
Author: imdorsww <shiravanifard@gmail.com>
Date:   Wed Jan 15 19:25:17 2025 +0330

    Revert "afzodan hoshdar eshtebah be script.js"

    This reverts commit 1e4e48efca9bf58108d637d04686d8c6625d90b6.

diff --git a/script.js b/script.js
index 719a6b9..dd10220 100644
--- a/script.js
+++ b/script.js
@@ -1,2 +1 @@
-console.log('به پروژه وب من خوش آمدید ');
-alert ('این یک هشداراشتباه است')
\ No newline at end of file
+console.log('به پروژه وب من خوش آمدید ');
\ No newline at end of file

C:\webproject>git remote add WebProject https://github.com/imdorsww/WebProject.git
error: remote WebProject already exists.

C:\webproject>git push -u WebProject master
info: please complete authentication in your browser...
Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 4 threads
Compressing objects: 100% (21/21), done.
Writing objects: 100% (21/21), 2.46 KiB | 419.00 KiB/s, done.
Total 21 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), done.
To https://github.com/imdorsww/WebProject.git
 * [new branch]      master -> master
branch 'master' set up to track 'WebProject/master'.

C:\webproject>git clone
fatal: You must specify a repository to clone.

usage: git clone [<options>] [--] <repo> [<dir>]

    -v, --[no-]verbose    be more verbose
    -q, --[no-]quiet      be more quiet
    --[no-]progress       force progress reporting
    --[no-]reject-shallow don't clone shallow repository
    -n, --no-checkout     don't create a checkout
    --checkout            opposite of --no-checkout
    --[no-]bare           create a bare repository
    --[no-]mirror         create a mirror repository (implies --bare)
    -l, --[no-]local      to clone from a local repository
    --no-hardlinks        don't use local hardlinks, always copy
    --hardlinks           opposite of --no-hardlinks
    -s, --[no-]shared     setup as shared repository
    --[no-]recurse-submodules[=<pathspec>]
                          initialize submodules in the clone
    --[no-]recursive ...  alias of --recurse-submodules
    -j, --[no-]jobs <n>   number of submodules cloned in parallel
    --[no-]template <template-directory>
                          directory from which templates will be used
    --[no-]reference <repo>
                          reference repository
    --[no-]reference-if-able <repo>
                          reference repository
    --[no-]dissociate     use --reference only while cloning
    -o, --[no-]origin <name>
                          use <name> instead of 'origin' to track upstream
    -b, --[no-]branch <branch>
                          checkout <branch> instead of the remote's HEAD
    -u, --[no-]upload-pack <path>
                          path to git-upload-pack on the remote
    --[no-]depth <depth>  create a shallow clone of that depth
    --[no-]shallow-since <time>
                          create a shallow clone since a specific time
    --[no-]shallow-exclude <revision>
                          deepen history of shallow clone, excluding rev
    --[no-]single-branch  clone only one branch, HEAD or --branch
    --no-tags             don't clone any tags, and make later fetches not to follow them
    --tags                opposite of --no-tags
    --[no-]shallow-submodules
                          any cloned submodules will be shallow
    --[no-]separate-git-dir <gitdir>
                          separate git dir from working tree
    --[no-]ref-format <format>
                          specify the reference format to use
    -c, --[no-]config <key=value>
                          set config inside the new repository
    --[no-]server-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
    --[no-]filter <args>  object filtering
    --[no-]also-filter-submodules
                          apply partial clone filters to submodules
    --[no-]remote-submodules
                          any cloned submodules will use their remote-tracking branch
    --[no-]sparse         initialize sparse-checkout file to include only files at root
    --[no-]bundle-uri <uri>
                          a URI for downloading bundles before fetching from origin remote


C:\webproject>C:\Users\HAMI>cd C:\webproject
'C:\Users\HAMI' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git init
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Initialized empty Git repository in C:/webproject/.git/
'Initialized' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git status
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>On branch master
'On' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>No commits yet
'No' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>Untracked files:
'Untracked' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  (use "git add <file>..." to include in what will be committed)
'use' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>        index.html

C:\webproject>        script.js

C:\webproject>        style.css


C:\webproject>
C:\webproject>nothing added to commit but untracked files present (use "git add" to track)
'nothing' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git add script.js style.css index.html
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git status
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>On branch master
'On' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>No commits yet
'No' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>Changes to be committed:
'Changes' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  (use "git rm --cached <file>..." to unstage)
'use' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>        new file:   index.html
'new' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>        new file:   script.js
'new' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>        new file:   style.css
'new' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>
C:\webproject>C:\webproject>git commit -m " avalin commit ba file haye js,css.html"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[master (root-commit) e26a4b3]  avalin commit ba file haye js,css.html
'[master' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> 3 files changed, 17 insertions(+)
'3' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> create mode 100644 index.html
'create' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> create mode 100644 script.js
'create' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> create mode 100644 style.css
'create' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git branch feature/update-title
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git branch
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  feature/update-title
'feature' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>* master
'*' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git checkout feature/update-title
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Switched to branch 'feature/update-title'
'Switched' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git status
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>On branch feature/update-title
'On' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Changes not staged for commit:
'Changes' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  (use "git add <file>..." to update what will be committed)
'use' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  (use "git restore <file>..." to discard changes in working directory)
'use' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>        modified:   index.html
'modified:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>no changes added to commit (use "git add" and/or "git commit -a")
'no' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git add index.html
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git commit -m"onvan dar index.html beroz resani shod"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[feature/update-title d77153a] onvan dar index.html beroz resani shod
The system cannot find the path specified.

C:\webproject> 1 file changed, 1 insertion(+), 1 deletion(-)
'1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git log
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>commit d77153a8afe5eb9d9888a2851035e2a9b7eb1fde (HEAD -> feature/update-title)
The system cannot find the path specified.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:03:09 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    onvan dar index.html beroz resani shod
'onvan' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit e26a4b3d3a1ae92641881754047d652effe1a0a1 (master)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 18:56:49 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>     avalin commit ba file haye js,css.html
'avalin' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git diff
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git checkout master
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Switched to branch 'master'
'Switched' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git merge feature/update-title
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Updating e26a4b3..d77153a
'Updating' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Fast-forward
'Fast-forward' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> index.html | 2 +-
'2' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> 1 file changed, 1 insertion(+), 1 deletion(-)
'1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git show
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>commit d77153a8afe5eb9d9888a2851035e2a9b7eb1fde (HEAD -> master, feature/update-title)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:03:09 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    onvan dar index.html beroz resani shod
'onvan' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>diff --git a/index.html b/index.html
'diff' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>index 116677b..d5a6ba8 100644
'index' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>--- a/index.html
'---' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>+++ b/index.html
'+++' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>@@ -1,7 +1,7 @@
'-1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> <!DOCTYPE html>
The syntax of the command is incorrect.

C:\webproject> <html>
The syntax of the command is incorrect.

C:\webproject> <head>
The syntax of the command is incorrect.

C:\webproject>-<title> پروژه وب من  </title>
The syntax of the command is incorrect.

C:\webproject>+<title>پروژه وب من بروزرسانی شد   </title>
The syntax of the command is incorrect.

C:\webproject> <link rel="stylesheet" href="style.css">
The syntax of the command is incorrect.

C:\webproject> </head>
The syntax of the command is incorrect.

C:\webproject> <body>
The syntax of the command is incorrect.

C:\webproject>
C:\webproject>C:\webproject>git branch -d feature/update-title
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Deleted branch feature/update-title (was d77153a).
'Deleted' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git branch feature/conflict-example
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git checkout feature/conflict-example
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Switched to branch 'feature/conflict-example'
'Switched' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject> git add index.html
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git commit -m"taghit dar h1 baraye ijad conflict"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[feature/conflict-example a2cee73] taghit dar h1 baraye ijad conflict
The system cannot find the path specified.

C:\webproject> 1 file changed, 1 insertion(+), 1 deletion(-)
'1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git show
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>commit a2cee7331b3c9bdb411bf003033f05eb6584b200 (HEAD -> feature/conflict-example)
The system cannot find the path specified.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:15:46 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    taghit dar h1 baraye ijad conflict
'taghit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>diff --git a/index.html b/index.html
'diff' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>index d5a6ba8..ad7d68b 100644
'index' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>--- a/index.html
'---' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>+++ b/index.html
'+++' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>@@ -5,7 +5,7 @@
'-5' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> <link rel="stylesheet" href="style.css">
The syntax of the command is incorrect.

C:\webproject> </head>
The syntax of the command is incorrect.

C:\webproject> <body>
The syntax of the command is incorrect.

C:\webproject>-<h1> به پروژه وب من خوش آمدید</h1>
The syntax of the command is incorrect.

C:\webproject>+<h1> این یک تغییر برای ایجاد conflict است</h1>
The syntax of the command is incorrect.

C:\webproject> <script src="script.js"></script>
< was unexpected at this time.

C:\webproject> </body>
The syntax of the command is incorrect.

C:\webproject> </html>
The syntax of the command is incorrect.

C:\webproject>\ No newline at end of file
'\' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git checkout master
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Switched to branch 'master'
'Switched' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git add index.html
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git commit -m"taghit dar h1 main baraye ijad conflict"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[master e9d3670] taghit dar h1 main baraye ijad conflict
'[master' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> 1 file changed, 1 insertion(+), 1 deletion(-)
'1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git merge feature/conflict-example
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Auto-merging index.html
'Auto-merging' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>CONFLICT (content): Merge conflict in index.html
'CONFLICT' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Automatic merge failed; fix conflicts and then commit the result.
'Automatic' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git add index.html
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git commit-m" conflict raf shod"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>git: 'commit-m conflict raf shod' is not a git command. See 'git --help'.
'git:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git status
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>On branch master
'On' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>All conflicts fixed but you are still merging.
'All' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  (use "git commit" to conclude merge)
'use' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>Changes to be committed:
'Changes' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>        modified:   index.html
'modified:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>
C:\webproject>C:\webproject>git commit -m " cnflict hal shod"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[master ee525c3]  cnflict hal shod
'[master' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git branch
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  feature/conflict-example
'feature' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>* master
'*' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git add script.js
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git commit -m "afzodan hoshdar eshtebah be script.js"
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[master 1e4e48e] afzodan hoshdar eshtebah be script.js
'[master' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> 1 file changed, 2 insertions(+), 1 deletion(-)
'1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git log
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>commit 1e4e48efca9bf58108d637d04686d8c6625d90b6 (HEAD -> master)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:24:30 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    afzodan hoshdar eshtebah be script.js
'afzodan' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit ee525c345c8e7ec4824ccf4cace91ee4cd63abf2
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Merge: e9d3670 a2cee73
'Merge:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:21:46 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>     cnflict hal shod
'cnflict' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit e9d3670ceab5dd421f734b5e6adf5f861672f0a3
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:17:50 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    taghit dar h1 main baraye ijad conflict
'taghit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit a2cee7331b3c9bdb411bf003033f05eb6584b200 (feature/conflict-example)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:15:46 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    taghit dar h1 baraye ijad conflict
'taghit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit d77153a8afe5eb9d9888a2851035e2a9b7eb1fde
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:03:09 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    onvan dar index.html beroz resani shod
'onvan' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit e26a4b3d3a1ae92641881754047d652effe1a0a1
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 18:56:49 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>     avalin commit ba file haye js,css.html
'avalin' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git revert  1e4e48efca9bf58108d637d04686d8c6625d90b6
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>[master f1e5d64] Revert "afzodan hoshdar eshtebah be script.js"
'[master' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> 1 file changed, 1 insertion(+), 2 deletions(-)
'1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git log
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>commit f1e5d6405cf88e3dbab79f1ae3078762f1246df1 (HEAD -> master)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:25:17 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    Revert "afzodan hoshdar eshtebah be script.js"
'Revert' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>    This reverts commit 1e4e48efca9bf58108d637d04686d8c6625d90b6.
'This' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit 1e4e48efca9bf58108d637d04686d8c6625d90b6
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:24:30 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    afzodan hoshdar eshtebah be script.js
'afzodan' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit ee525c345c8e7ec4824ccf4cace91ee4cd63abf2
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Merge: e9d3670 a2cee73
'Merge:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:21:46 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>     cnflict hal shod
'cnflict' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit e9d3670ceab5dd421f734b5e6adf5f861672f0a3
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:17:50 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    taghit dar h1 main baraye ijad conflict
'taghit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit a2cee7331b3c9bdb411bf003033f05eb6584b200 (feature/conflict-example)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:15:46 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    taghit dar h1 baraye ijad conflict
'taghit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit d77153a8afe5eb9d9888a2851035e2a9b7eb1fde
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:03:09 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    onvan dar index.html beroz resani shod
'onvan' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>commit e26a4b3d3a1ae92641881754047d652effe1a0a1
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 18:56:49 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>     avalin commit ba file haye js,css.html
'avalin' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git show f1e5d6405cf88e3dbab79f1ae3078762f1246df1
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>commit f1e5d6405cf88e3dbab79f1ae3078762f1246df1 (HEAD -> master)
'commit' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Author: imdorsww <shiravanifard@gmail.com>
The syntax of the command is incorrect.

C:\webproject>Date:   Wed Jan 15 19:25:17 2025 +0330
The system cannot accept the date entered.
Enter the new date: (mm-dd-yy)

C:\webproject>    Revert "afzodan hoshdar eshtebah be script.js"
'Revert' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>    This reverts commit 1e4e48efca9bf58108d637d04686d8c6625d90b6.
'This' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>diff --git a/script.js b/script.js
'diff' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>index 719a6b9..dd10220 100644
'index' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>--- a/script.js
'---' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>+++ b/script.js
'+++' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>@@ -1,2 +1 @@
'-1' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>-console.log('به پروژه وب من خوش آمدید ');
'-console.log' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>-alert ('این یک هشداراشتباه است')
'-alert' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>\ No newline at end of file
'\' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>+console.log('به پروژه وب من خوش آمدید ');
'+console.log' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>\ No newline at end of file
'\' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git branch
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>  feature/conflict-example
'feature' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>* master
'*' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git remote add WebProject https://github.com/imdorsww/WebProject.git
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git push -u WebProject
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>fatal: The current branch master has no upstream branch.
'fatal:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>To push the current branch and set the remote as upstream, use
'To' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>    git push --set-upstream WebProject master
To https://github.com/imdorsww/WebProject.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/imdorsww/WebProject.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

C:\webproject>
C:\webproject>To have this happen automatically for branches without a tracking
'To' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>upstream, see 'push.autoSetupRemote' in 'git help config'.
'upstream' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>
C:\webproject>C:\webproject>git push -U WebProject
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>error: unknown switch `U'
'error:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>usage: git push [<options>] [<repository> [<refspec>...]]
The system cannot find the file specified.

C:\webproject>
C:\webproject>    -v, --[no-]verbose    be more verbose
'-v' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -q, --[no-]quiet      be more quiet
'-q' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]repo <repository>
The syntax of the command is incorrect.

C:\webproject>                          repository
'repository' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]all            push all branches
'--[no-]all' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]branches       alias of --all
'--[no-]branches' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]mirror         mirror all refs
'--[no-]mirror' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -d, --[no-]delete     delete refs
'-d' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]tags           push tags (can't be used with --all or --branches or --mirror)
'--[no-]tags' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -n, --[no-]dry-run    dry run
'-n' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]porcelain      machine-readable output
'--[no-]porcelain' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -f, --[no-]force      force updates
'-f' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]force-with-lease[=<refname>:<expect>]
The system cannot find the file specified.

C:\webproject>                          require old value of ref to be at this value
'require' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]force-if-includes
'--[no-]force-if-includes' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>                          require remote updates to be integrated locally
'require' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]recurse-submodules (check|on-demand|no)
'--[no-]recurse-submodules' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>                          control recursive pushing of submodules

C:\webproject>    --[no-]thin           use thin pack
'--[no-]thin' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]receive-pack <receive-pack>
The syntax of the command is incorrect.

C:\webproject>                          receive pack program
'receive' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]exec <receive-pack>
The syntax of the command is incorrect.

C:\webproject>                          receive pack program
'receive' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -u, --[no-]set-upstream
'-u' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>                          set upstream for git pull/status
Environment variable upstream for git pull/status not defined

C:\webproject>    --[no-]progress       force progress reporting
'--[no-]progress' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]prune          prune locally removed refs
'--[no-]prune' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --no-verify           bypass pre-push hook
'--no-verify' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --verify              opposite of --no-verify
'--verify' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]follow-tags    push missing but relevant tags
'--[no-]follow-tags' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]signed[=(yes|no|if-asked)]
'--[no-]signed[' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>                          GPG sign the push
'GPG' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    --[no-]atomic         request atomic transaction on remote side
'--[no-]atomic' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -o, --[no-]push-option <server-specific>
The syntax of the command is incorrect.

C:\webproject>                          option to transmit
'option' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -4, --ipv4            use IPv4 addresses only
'-4' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>    -6, --ipv6            use IPv6 addresses only
'-6' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>
C:\webproject>C:\webproject>git remote add WebProject https://github.com/imdorsww/WebProject.git
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>error: remote WebProject already exists.
'error:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>C:\webproject>git push -u WebProject master
'C:\webproject' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>info: please complete authentication in your browser...
'info:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Enumerating objects: 21, done.
'Enumerating' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Counting objects: 100% (21/21), done.
'Counting' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Delta compression using up to 4 threads
'Delta' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Compressing objects: 100% (21/21), done.
'Compressing' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Writing objects: 100% (21/21), 2.46 KiB | 419.00 KiB/s, done.
'Writing' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>Total 21 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
'Total' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>remote: Resolving deltas: 100% (6/6), done.
'remote:' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>To https://github.com/imdorsww/WebProject.git
'To' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject> * [new branch]      master -> master
'*' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>branch 'master' set up to track 'WebProject/master'.
'branch' is not recognized as an internal or external command,
operable program or batch file.

C:\webproject>
C:\webproject>git clone https://github.com/imdorsww/WebProject.git
Cloning into 'WebProject'...
remote: Enumerating objects: 25, done.
remote: Counting objects: 100% (25/25), done.
remote: Compressing objects: 100% (18/18), done.
remote: Total 25 (delta 8), reused 23 (delta 7), pack-reused 0 (from 0)
Receiving objects: 100% (25/25), done.
Resolving deltas: 100% (8/8), done.


