中山大学自动健康申报docker版本
只需根目录配置config.json文件后
即配置~/config.json文件
config.json配置如下
```
[
    {
        "method":"email",
        "username": "你的NETID",
        "password": "你的密码",
        "mail_host": "smtp.qq.com",
        "mail_user":"用来发送邮件的邮箱",
        "mail_token": "邮箱授权token",
        "mail_receiver": "用来接收邮件的邮箱",
        "wxsend_key":""
    },
    {
        "username": "别填",
        "password": "别填"
    }
]

```

然后在装好docker的机器上运行下列代码即可

```
docker run -d --name bskj -id -v /root/config.json:/config.json sysuyyds/bskj_usys:latest
```
