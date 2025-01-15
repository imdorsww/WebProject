


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

C:\webproject>git clone https://github.com/imdorsww/WebProject.git
