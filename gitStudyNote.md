**Git——学习笔记**

---

[toc]

---

# 1 Git 的基本使用

## 1.1 基本配置

- git 的全局用户名及邮箱配置：

  ```
  git config --globel user.name "在这个双引号内写入 用户名 如：lonxt"
  git config --globel user.email "同样地，写入邮箱地址如：longxt666@gamil.com"
  ```

- git 的初始化：进入一个文件夹执行 `git init` 即可，该命令将在当前文件夹下生成一个 `.git` 文件夹，里面存放了已经生成了的仓库的配置信息。

## 1.2 简单命令

> 假设当前文件夹下有一个 `readme.txt` 文件，用来进行辅助说明。

- 将当前仓库所在文件夹下的一个文件交给仓库去进行版本管理：`git add 文件名` 这里对应的就是 `git add readme.txt`。

  - 此后，该文件便在此仓库中正式存在了，否则的话，即使在同一个文件夹下，仓库也不会对其进行版本管理。

- 刚才用 `add` 命令将文件放入仓库了，但是仓库还没有把它进行注册，现在使用 `git commit -m "描述"` 来完成登记过程，如：`git commit -m "我把readme.txt文件进行了版本控制"`。

  - 可以一次放入多个文件：

    - ```
      git add file1.txt file2.txt
      git add file3.txt
      git commit -m "放入了3个文件，现在将它们放到货架上进行管理吧"
      ```

- 使用 `git status` 查看当前仓库的状态：

  - ![image-20200808084252842](/home/bruce_dragon/文档/myNote/git-learning/image-20200808084252842.png)

- 组合命令使用案例（1）：修改文件后查看状态及文件修改内容：

  - ![image-20200808085415339](/home/bruce_dragon/文档/myNote/git-learning/image-20200808085415339.png)
  - `diff` 命令仅在当前仓库状态存在红色的未更新的文本记录时才能生效。

- 组合命令使用案例（2）：

  - ![image-20200808085713591](/home/bruce_dragon/文档/myNote/git-learning/image-20200808085713591.png)
  - 以上可以看出，当 `git status` 获取当前仓库状态时，如果显示文件为红色则表示需要进行提交来更新文本信息，然后才能使用 `commit` 进行提交管理。

