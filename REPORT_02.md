#第2回　Webエンジニアリング演習　レポート
## 学籍番号
4724130
## コンフリクトが発生した理由
同じmainの2つのブランチ（practice/conflict-aとpractice/conflict-b）で同じ行の変更をしようとしたため、競合になってしまうから。
## 解決手順
##　履歴
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git add README.md
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git commit -m"Update goal in conflict B"
[practice/conflict-b 8e9ba5c] Update goal in conflict B
 1 file changed, 1 insertion(+), 1 deletion(-)
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git push -u origin practice/conflict-b
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 327 bytes | 327.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/4724130/web-eng-report
   8779c43..8e9ba5c  practice/conflict-b -> practice/conflict-b
branch 'practice/conflict-b' set up to track 'origin/practice/conflict-b'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git switch practic
e/conflict-a
Switched to branch 'practice/conflict-a'
Your branch is up to date with 'origin/practice/conflict-a'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git add README.md
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git commit -m "Update goal in conflict A"
[practice/conflict-a ffae02b] Update goal in conflict A
 1 file changed, 1 insertion(+), 1 deletion(-)
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git push -u origin practice/conflict-a
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/4724130/web-eng-report
   8779c43..ffae02b  practice/conflict-a -> practice/conflict-a
branch 'practice/conflict-a' set up to track 'origin/practice/conflict-a'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git switch practic
e/conflict-b
Switched to branch 'practice/conflict-b'
Your branch is up to date with 'origin/practice/conflict-b'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git pull --no-rebase origin main
From https://github.com/4724130/web-eng-report
 * branch            main       -> FETCH_HEAD
Already up to date.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git switch practice/conflict-a
Switched to branch 'practice/conflict-a'
Your branch is up to date with 'origin/practice/conflict-a'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git switch practice/conflict-b
Switched to branch 'practice/conflict-b'
Your branch is up to date with 'origin/practice/conflict-b'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git pull --no-rebase origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 897 bytes | 897.00 KiB/s, done.
From https://github.com/4724130/web-eng-report
 * branch            main       -> FETCH_HEAD
   8779c43..0cb1b9c  main       -> origin/main
Updating 8e9ba5c..0cb1b9c
Fast-forward
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-b) $ git switch practice/conflict-a
Switched to branch 'practice/conflict-a'
Your branch is up to date with 'origin/practice/conflict-a'.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git pull --no-rebase origin main
From https://github.com/4724130/web-eng-report
 * branch            main       -> FETCH_HEAD
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git status
On branch practice/conflict-a
Your branch is up to date with 'origin/practice/conflict-a'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git add README.md
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git commit -m "Resolve README conflict"
[practice/conflict-a c6344e1] Resolve README conflict
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/4724130/web-eng-report
   ffae02b..c6344e1  practice/conflict-a -> practice/conflict-a
@4724130 ➜ /workspaces/web-eng-report (practice/conflict-a) $ git switch main
Switched to branch 'main'
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)
@4724130 ➜ /workspaces/web-eng-report (main) $ git pull origin main
From https://github.com/4724130/web-eng-report
 * branch            main       -> FETCH_HEAD
Updating 8779c43..0cb1b9c
Fast-forward
 README.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)