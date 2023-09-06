# Command list

```
git config --global user.name "hoang-emperor"
git config --global user.email "hoangdepzai0001@gmail.com"
```
Dùng để cho Git biết bạn là ai, dùng tương ứng tên bạn và mail trên GitHub.


```
git init
```
Dùng để khởi tạo Git trong thư mục đó

```
git add [file_name] //dùng để stage 1 file nhất định

hoặc

git add --all //dùng để stage all file trong folder đó
git add -A 
```

```
git status
```
Dùng để check trạng thái các file trong folder
```
git commit -m "Bla bla"
```
Dùng để làm checkpoint 
Note: Short status flags are:

?? - Untracked files<br>
A - Files added to stage<br>
M - Modified files<br>
D - Deleted files<br>

```
git log
```
Xem history git commit

```
git (command) -help //Dùng để hiện help lệnh cụ thể (chi tiết)

or 

git help --all // Dùng để hiện mô tả tất cả các lệnh
```

```
git branch <name_branch> //Tạo 1 nhánh mới
```

```
git branch //liệt kê các nhánh, nhánh có prefix * là nhánh chính
```

```
git checkout <branch_name> //Switch tới nhánh branch_name
```

## Emergency Branch

```
git checkout -b emergency-fix
```
Now imagine that we are not yet done with hello-world-images, but we need to fix an error on master.

I don't want to mess with master directly, and I do not want to mess with hello-world-images, since it is not done yet.

So we create a new branch to deal with the emergency. <br>

**Note**: Using the -b option on checkout will create a new branch, and move to it, if it does not exist


## Merge branch
We have the emergency fix ready, and so let's merge the master and emergency-fix branches.

First, we need to change to the master branch:
```
git checkout master
git merge emergency-fix
```

Since the emergency-fix branch came directly from master, and no other changes had been made to master while we were working, Git sees this as a continuation of master. So it can "Fast-forward", just pointing both master and emergency-fix to the same commit.

As master and emergency-fix are essentially the same now, we can delete emergency-fix, as it is no longer needed:
```
git branch -d emergency-fix
```


Việc làm cũng tương tự nếu nhánh không từ main mà ra, nhưng khi merge sẽ phải check sự thay đổi, maybe sinh ra lỗi nếu 2 file có sự khác nhau

## Work with Github

### Git fetch
fetch gets all the change history of a tracked branch/repo.

So, on your local Git, fetch updates to see what has changed on GitHub:
```
git fetch origin  //after that, use git status to see the changes
```

### Git pull
pull is a combination of fetch and merge. It is used to pull all changes from a remote repository into the branch you are working on.
```
git pull origin
```


### Git push
```
git remote add origin <link_repo>
git push --set-upstream origin master

```