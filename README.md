توضیحات پروژه

   پروژه در مسیر C:\webproject با استفاده از دستور git init ایجاد شد.

   فایل‌های index.html، style.css و script.js اضافه شده و اولین commit با پیام "avalin commit ba file haye js,css.html" ذخیره شد.

   شاخه‌ای با نام feature/update-title ساخته شد و تغییرات در فایل index.html اعمال و ذخیره شدند. سپس این شاخه به شاخه اصلی master ادغام شد.

   یک conflict در فایل index.html بین دو شاخه ایجاد شد که پس از ویرایش، مشکل حل و تغییرات ذخیره شد.

   تغییر اشتباهی در فایل script.js ذخیره شده بود که با استفاده از دستورgit revert این تغییر به حالت قبلی برگشت داده شد.

   پروژه به مخزن GitHub متصل و فایل‌ها با دستور git push آپلود شدند.



 git init
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


