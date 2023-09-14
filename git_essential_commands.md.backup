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
### Git add
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
Dùng để làm checkpoint <br>
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
### Git branch
```
git branch <name_branch> //Tạo 1 nhánh mới
```

```
git branch //liệt kê các nhánh, nhánh có prefix * là đang xét
```

```
git branch -r // xem nhánh các nhánh từ các remote repo
```


### Git checkout
```
git checkout <branch_name> //Switch tới nhánh branch_name
```


```
git checkout -b <branch_name>
```

Áp dụng tham số -b sẽ tạo một nhánh mới và chuyển ngay đến nhánh đó (kết hợp giữa 2 lệnh `git branch <branch_name> && git checkout <branch_name>`)

```
git checkout -b ＜new-branch＞ ＜existing-branch＞
```

Trong tổng thể, nếu bạn thực hiện lệnh `git branch` thì git sẽ liệt kê hết các branch ở `HEAD` ra, nhưng nếu bạn thực hiện lệnh bên dưới, từ nhánh <existing_branch> bạn lại phân ra 1 nhánh mới, giống như từ 1 thân cây -> nhiều nhánh cây -> nhiều nhánh con.

### Git remote

```
git remote
```

Liệt kê tất cả các remote của các repo mà bạn đang có.

```
git remote -v
```
Giống `git remote` nhưng có thêm link URL
```
git remote add <name> <url>
```
Tạo 1 kết nối mới đến link url, sau khi thực hiện lệnh bạn có thể dùng `name` như là 1 shortcut cho `url`

```
git remote rm <name>
```
Bỏ kết nối tới repo `name`
```
git remote rename <old-name> <new-name>
```
đặt lại tên remote connection

```
git remote show <name>
```
Hiện 1 list nhánh liên quan đến remote `name` đó và các điểm cuối để fetch and push

### Git clone
Git clone sẽ tạo 1 kết nối remote ở repo mà bạn clone về.

### Git push
Dùng để write to the remote repo

```
git push <remote-name> <branch-name>
```

Command trên dùng để update trạng thái hiện tại của `branch-name` lên remote repo `remote-name`

### Git fetch
```
git fetch <remote>
```

Lấy tất cả các nhánh từ repo `remote`

```
git fetch <remote> <branch>
```
Chỉ lấy từ `branch`

```
git fetch --all
```
Lấy tất cả từ các registered remotes 

```
git fetch --dry-run
```
Thực hiện thử chạy lệnh fetch, nó sẽ hiển thị tất cả các hành động trong quá trình fetch nhưng không áp dụng chúng.

```
git fetch origin
```
hiển thị tất cả các nhánh đã được download