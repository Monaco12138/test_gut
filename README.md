# Git 使用
1. 从Github上创建一个项目，默认的分支是/main；
    ```shell
    git init #默认分支是/master
    git init -b main #可以修改默认分支为/main
    ```

2. 从本地init一个分支为例，在本地进行操作修改后如何同步到Github上对应的项目
   如果本地分支为main：
   ```shell
   #先pull下Github上对应的空白内容，主要是同步历史
   git pull origin main --allow-unrelated-histories

   #接着就可以正常操作，本地和Github上项目已经同步 
    ```