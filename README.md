#gitが入っているかの確認
(base) odakana@odakanas-MacBook-Air ~ % git --version
git version 2.32.1 (Apple Git-13

#Desktopにファイルを作成
(base) odakana@odakanas-MacBook-Air ~ % cd ~/Desktop

#git上のリモートリポジトリをローカル上でクローンする
(base) odakana@odakanas-MacBook-Air Desktop % git clone https://github.com/ka71279/my-first-repo3.git
Cloning into 'my-first-repo3'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Receiving objects: 100% (3/3), done.d
Receiving objects: 100% (3/3), done

＃Desktop上のファイルリスト一覧ファイルが作成されていることを確認
(base) odakana@odakanas-MacBook-Air Desktop % ls
my-first-repo3

＃作成したファイルの中身のリストを確認
(base) odakana@odakanas-MacBook-Air Desktop % cd my-first-repo3
(base) odakana@odakanas-MacBook-Air my-first-repo3 % ls
README.md

＃ローカルとリモートリポジトリの認識部分の確認
(base) odakana@odakanas-MacBook-Air my-first-repo3 % ls -a
.		..		.git		README.md

＃ユーザーの設定
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git config user.name 'ka712
79'
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git config user.email 'o.00
59.kana@gmail.com'
(base) odakana@odakanas-MacBook-Air my-first-repo3 % cd ~/Desktop/my-first-repo3

＃今いるリポジトリの場所を確認
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git branch
* main
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git checkout -b update-read
me
Switched to a new branch 'update-readme'
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git branch
  main
* update-readme
(base) odakana@odakanas-MacBook-Air my-first-repo3 % subl README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git status
On branch update-readme
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git add README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git status
On branch update-readme
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   README.md

(base) odakana@odakanas-MacBook-Air my-first-repo3 % git commit -m 'update read
me'
[update-readme a30b9fb] update read me
 1 file changed, 2 insertions(+), 1 deletion(-)
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git status
On branch update-readme
nothing to commit, working tree clean
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git log
commit a30b9fb942a774352b30d57648a1b930f0f5d57e (HEAD -> update-readme)
Author: ka71279 <o.0059.kana@gmail.com>
Date:   Mon Jul 11 20:04:36 2022 +0900

    update read me

commit 62bb1294ec12314aaafc27d0569e6f7949207b8d (origin/main, origin/HEAD, main)
Author: ka71279 <109014111+ka71279@users.noreply.github.com>
Date:   Mon Jul 11 19:52:12 2022 +0900

    Initial commit
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
(base) odakana@odakanas-MacBook-Air my-first-repo3 % my-first-repo3
zsh: command not found: my-first-repo3
(base) odakana@odakanas-MacBook-Air my-first-repo3 % subl README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git pull origin master
fatal: couldn't find remote ref master
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git pull origin main
From https://github.com/ka71279/my-first-repo3
 * branch            main       -> FETCH_HEAD
Already up to date.
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git push origin update-read
me
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 276 bytes | 276.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'update-readme' on GitHub by visiting:
remote:      https://github.com/ka71279/my-first-repo3/pull/new/update-readme
remote:
To https://github.com/ka71279/my-first-repo3.git
 * [new branch]      update-readme -> update-readme
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git pull origin master
fatal: couldn't find remote ref master
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git pull origin main
From https://github.com/ka71279/my-first-repo3
 * branch            main       -> FETCH_HEAD
Already up to date.
(base) odakana@odakanas-MacBook-Air my-first-repo3 % subl README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git pull origin main
From https://github.com/ka71279/my-first-repo3
 * branch            main       -> FETCH_HEAD
Already up to date.
(base) odakana@odakanas-MacBook-Air my-first-repo3 % subl README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 % subl README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 % git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 623 bytes | 207.00 KiB/s, done.
From https://github.com/ka71279/my-first-repo3
 * branch            main       -> FETCH_HEAD
   62bb129..cab4a29  main       -> origin/main
Updating 62bb129..cab4a29
Fast-forward
 README.md | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
(base) odakana@odakanas-MacBook-Air my-first-repo3 % subl README.md
(base) odakana@odakanas-MacBook-Air my-first-repo3 %
