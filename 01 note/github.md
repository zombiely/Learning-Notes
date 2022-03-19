# github note

## license chose  

### 选择 license

![license](..\images\license chose.jpg)

## 安装git  

下载传送门
<https://npm.taobao.org/mirrors/git-for-windows/>

选择版本
进入后，选择你想要的版本，它里面是 降序排序。

## vs-code项目同步到github上的两种方法

* 方法一：复制法
在github上创建一个repository
复制这个repository的地址，在Terminal上执行git clone + 地址的指令
在这里插入图片描述
在这里插入图片描述
3.此时vue文件夹中就会出现一个相应的新的文件夹，把要导入的文件的信息复制到新的文件夹
在这里插入图片描述
4.在Terminal中依次执行 以下命令

```git
git add .
  
git commit -m "初始化项目"
```

这时回到自己的github仓库刷新，就可以看到已经更新的文件。

* 方法二
在github上创建一个repository,复制地址
在要导入github的文件夹的目录下，执行以下指令

```git
git remote add origin https://github.com/zombiely/Learning-Notes

git push -u origin master
```

这时回到自己的github仓库刷新，就可以看到已经更新的文件。
