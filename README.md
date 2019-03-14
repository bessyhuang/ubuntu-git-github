# ubuntu-git-github

## Ubuntu 操作

### 1. 先有 Github 帳戶，並 Create a new repository，點擊 Clone or download 中 Clone with HTTPS 的 URL，先把它複製下來。
`github基本教學 - 從無到有` https://www.youtube.com/watch?v=py3n6gF5Y00


### 2. Ubuntu 安裝 Git https://git-scm.com/download/linux
`How to Install and Configure Git and GitHub on Ubuntu 18.04 (Linux)` https://www.youtube.com/watch?v=ZMgLZUYd8Cw
   
* 開啟終端機輸入以下指令：
```
sudo apt-get install git
git --version
git config --global user.name "GitHub 帳戶的帳號"
git config --global user.email "GitHub 帳戶的信箱"
```

### 3. 要產生 SSH keys 才能和 Github 帳戶做配對
`git 1: SSH keys for KTH GitHub` https://www.youtube.com/watch?v=Sp5AASmX4no&index=46&t=0s&list=WL
  
* 先開啟終端機輸入以下指令：
```
ssh-keygen -t rsa -b 4096 -C "你註冊的電子信箱"
ls  ~/.ssh
cat ~/.ssh/id_rsa.pub           -> 會產生金鑰，把它複製下來。
```

* 接著到 Github 帳戶 -> Settings -> SSH keys -> New SSH keys -> 把產生的金鑰貼上，並命名。
  
* 如何確定是否連上，開啟終端機輸入以下指令：
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa       -> 會出現 Identity added: /home/testchia/.ssh/id_rsa (/home/testchia/.ssh/id_rsa)
```
### 4. 配對完後，如何開始利用它來做事，操作如下：

* 開啟終端機輸入以下指令：
```
mkdir git_workspace     ->在電腦上建立工作資料夾
cd git_workspace
git clone https://github.com/bessyhuang/django-personalsite.git   ->這裡的 URL 就是步驟1.的時候所產生的 URL。
```

* 接下來就可以在這個資料夾底下放東西，如程式碼，之後再把它傳上雲端的 Github 就可以了。

### 5. 先用終端機再進入該資料夾，進而把它傳上雲端的 Github 帳戶中。
* 開啟終端機輸入以下指令：
```
cd django-personalsite
git status
git add "你新增的東西"
git status
git commit -m "註記"
git push origin master     -> 上傳 Github 
```
---

## 【分支】使用教學：http://tech-marsw.logdown.com/blog/2013/08/16/git-notes-github

### 1. 本機端初始化
> sudo apt-get install git-all

> git config --global user.name "chia"

> git config --global user.email "404040523@gapp.fju.edu.tw"

> git clone https://github.com/bessyhuang/myaccounts.git

> cd myaccounts/

### 2. 生一個新branch名叫v1
> git branch v1

### 3. 切換到v1這個branch上
> git checkout v1

### 4. ~~ 開始來寫code啦!!! 隨意修改增刪檔案 ~~

### 5. 看修改了哪些檔案
> git status

> git add --all

> git status

> git commit -m "Change from SQLite to MySQL"  //註解要寫清楚 完成一個小功能就要commit一次

### 6. 合併->push到Github上
> git checkout master

### 7. 把v1和master merge起來
> git merge v1

### 8. 接著輸入Github的帳號密碼，同步到Github上了
> git push
