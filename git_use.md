## 上传文件

1. 全部上传

```git
$ git add .
# 把本地仓库的文件上传到缓存
$ git commit -m 'something new add'
# 提交，-m 接注释，就是本次文件的说明

#可能会进行身份验证,不用则跳过
$ git config --global user.email '976510632@qq.com'   
# 验证email
$ git config --global user.name '976510632'    
# 验证name

$ git remote add origin git@github.com:976510632/CODER_CLASS.git    
# 填写上传到的项目地址 
$ git push origin master    
# 推送到项目里
```

2. 某个文件上传

```git
$ git add 1.txt    
# 上传1.txt，同上后续
```

## 删除文件

1. 同时删除本地和GIT里的某个文件

```git
# 直接在本地文件夹删除某个文件，然后打开Bash
$ git add .
# 把本地仓库的文件上传到缓存
$ git commit -m 'del somthing'
# 提交，-m 接注释，就是本次文件的说明
$ git push -u origin master
# 推送到项目里
```

2. 删除GIT某个项目里的某个文件，但本地项目文件不改动

```git
# 这两步好像有用，略去也可以
$ git pull origin master
# 将远程仓库里面的项目拉下来到本地文件夹,可拉可不拉
$ dir
# 查看是不是有文件

$ git rm -r --cached 1.txt
# 删除1.txt
$ git commit -m 'del 1.txt'
# 提交，-m 接注释，就是本次文件的说明
$ git push -u origin master
# 推送到项目里
```
