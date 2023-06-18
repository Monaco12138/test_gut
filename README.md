# Git 使用


- 从Github上创建一个项目，默认的分支是/main；
    ```shell
    git init #默认分支是/master
    git init -b main #可以修改默认分支为/main
    ```

- 本地创建项目后连接到Github上
   ```shell
   #先在Github上创建相应的项目，复制对应的ssh链接(需要将本地的ssh 公钥拷贝到Github设置中)
   git remote add origin git@github.com:Monaco12138/xxx

   #输入下面指令查看连接情况
   git remote -v
   ```

- 从本地init一个分支为例，在本地进行操作修改后如何同步到Github上对应的项目
   __如果本地分支为main：__
   ```shell
   #先pull下Github上对应的空白内容，主要是同步历史
   git pull origin main --allow-unrelated-histories

   #接着就可以正常操作，本地和Github上项目已经同步 
    ```

   __如果本地分支为master:__
    - 可以创建一个新的main分支进行操作
        ```shell
        git branch <branch name> #创建新分支

        git checkout <branch name> #切换分支
        ```
    