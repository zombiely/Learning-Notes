## 邮件别名
config文件
[/etc/postfix/main.config](mail\config file\main.cf)

1.编辑别名文件

vim /etc/aliases
内容：

jack:rose

如果要转发到多个，则为：

jack:rose,coco


2.修改/etc/postfix/main.cf，一般都有，检查一下，没有就加上

alias_maps = hash:/etc/aliases
alias_database = hash:/etc/aliases

3.应用修改，分别执行如下命令

postalias /etc/aliases          
postfix reload

4.配置完成，测试往jack@test.com发送邮件，结果rose@test.com能收到。


我这里主要是实现让外部邮件都到rose@test.com邮箱，然后做相应的邮件内容提取。
