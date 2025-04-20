# Learning Git and GitHub
YA -20250420

<br>

# Steps
1. 在vscode終端機輸入使用者名稱和Email
```sh
git config --global user.name "cy"
git config --global user.email "alisawang09@gmail.com"
```
2. 開始git
```sh
git init
```
3. 建立 .gitignore檔案，寫入想避免上傳的檔案
    - 例如：*.png，代表上傳會忽略所有 png
    - 一行個資料，也可以寫整個資料夾：folder/
4. 將全部檔案上傳到暫存區
```sh
git add .
```
5. Commit上傳
```sh
git commit -m "打上commit備註"
```
6. 如果要刪除文件，要在 add 那個檔案，然後再 commit，status就會乾淨
    - 也可以用下面指令一次add, commit (但不適用新建的檔案)
    ```sh 
    git commit -am　"message"
    ```

<br>

7. 在 GitHub建立 Repository，回到vscode在終端機輸入GitHub上的指令

<br>

8. 之後如果有更動檔案，除了要 add 和 commit 之外，還要再輸入下面才會傳到github上
```sh
git push
```
<br>

# Collaboration
1. 在github Setting加入協作者
2. 協作者複製網址，到自己的vscode終端機輸入
```sh
git clone 網址
```
3. 之後要pull新的資料 (版本)，就輸入
```sh
git pull
```

<br>

# Commands
```sh
#檢查狀態
git status

#檢查版本
git --version

#清空終端機
clear

#顯示提交(commit)歷史，按q退出
git log
git log --oneline

#檢查檔案差別
git diff 版本號碼 -- 檔名

#回復檔案到某檢查點 (也需要再commit)
git checkout 版本號碼 -- 檔名
#回復到某檢查點，並刪除之後的紀錄 (不可逆)
git reset --hard 版本號碼
```

<br>

# Branch
```sh
#查看目前分支
git branch -v

#建立新分支
git branch newbranch

#切換與建立新的newbranch
git checkout -b newbranch

#切換到newbranch分支
git checkout newbranch

#刪除分支
git branch -d newbranch

#push分支的東西
git push origin newbranch
#會在github的pullrequest看到

#合併newbranch到主分支
git merge newbranch
```