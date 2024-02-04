# GitLab部署

> 作者：hipython2023
>
> 说明：该文档的部署系统为 **Ubuntu**
>
> 尊重项目原创性！

## 查看系统版本

~~~sh
lsb_release -a
~~~

## 下载安装包

官网地址：https://packages.gitlab.com/gitlab/gitlab-ce

以 **Ubuntu/jammy** 为例：

~~~sh
wget https://packages.gitlab.com/gitlab/gitlab-ce/packages/ubuntu/jammy/gitlab-ce_16.7.0-ce.0_amd64.deb/download.deb
~~~

## 安装GitLab依赖

~~~sh
sudo apt-get install -y curl openssh-server ca-certificates
~~~

~~~sh
sudo apt-get install -y postfix
~~~

## 安装

~~~sh
sudo dpkg -i downloal.deb
~~~

编辑文件

~~~sh
vim /etc/gitlab/gitlab.rb
~~~

重新启动GitLab

~~~ sh
sudo gitlab-ctl reconfigure
~~~

## 修改root密码

~~~~sh
sudo gitlab-rails console
~~~~

~~~ sh
user=User.where(id:1).first 
user.password='密码'
user.password_confirmation='密码' 
user.save! 
quit
~~~

**重启服务器！！！**

