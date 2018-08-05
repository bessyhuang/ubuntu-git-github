# django-personalsite
django 個人網頁

>>  Ubuntu 操作

1.先有 Github 帳戶，並 Create a new repository，點擊 Clone or download 中 Clone with HTTPS 的 URL，先把它複製下來。
  github基本教學 - 從無到有
  https://www.youtube.com/watch?v=py3n6gF5Y00

2.（要產生 SSH keys 才能和 Github 帳戶做配對）
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

3.產生 SSH keys 才能和 Github 帳戶做配對



2.
  How to Install and Configure Git and GitHub on Ubuntu 18.04 (Linux)
  https://www.youtube.com/watch?v=ZMgLZUYd8Cw
