# django-personalsite
django 個人網頁

>>  Ubuntu 操作

1. 先有 Github 帳戶，並 Create a new repository，點擊 Clone or download 中 Clone with HTTPS 的 URL，先把它複製下來。
      github基本教學 - 從無到有
      https://www.youtube.com/watch?v=py3n6gF5Y00


2. Ubuntu 安裝 Git 
      https://git-scm.com/download/linux
      
      How to Install and Configure Git and GitHub on Ubuntu 18.04 (Linux)
      https://www.youtube.com/watch?v=ZMgLZUYd8Cw
   
   開啟終端機輸入以下指令：
      sudo apt-get install git
      git --version
      git config --global user.name "GitHub 帳戶的帳號"
      git config --global user.email "GitHub 帳戶的信箱"


3. 要產生 SSH keys 才能和 Github 帳戶做配對
      git 1: SSH keys for KTH GitHub
      https://www.youtube.com/watch?v=Sp5AASmX4no&index=46&t=0s&list=WL
  
    先開啟終端機輸入以下指令：
      ssh-keygen -t rsa -b 4096 -C "你註冊的電子信箱"
      ls  ~/.ssh
      cat ~/.ssh/id_rsa.pub           ->會產生金鑰，把它複製下來。
  
    接著到 Github 帳戶 -> Settings -> SSH keys -> New SSH keys -> 把產生的金鑰貼上，並命名。
  
    如何確定是否連上，開啟終端機輸入以下指令：
      eval "$(ssh-agent -s)"
      ssh-add ~/.ssh/id_rsa       ->  會出現 Identity added: /home/testchia/.ssh/id_rsa (/home/testchia/.ssh/id_rsa)

4. 配對完後，如何開始利用它來做事，操作如下：
      開啟終端機輸入以下指令：
            mkdir git_workspace     ->在電腦上建立工作資料夾
            cd git_workspace
            git clone https://github.com/bessyhuang/django-personalsite.git   ->這裡的 URL 就是步驟1.的時候所產生的 URL。
            
      接下來就可以在這個資料夾底下放東西，如程式碼，之後再把它傳上雲端的 Github 就可以了。

5.
  
