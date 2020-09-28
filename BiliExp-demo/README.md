## Bilibili 自动签到模版

### 项目说明
本项目为您提供了基于腾讯云云函数部署的B站定时签到模版

### 部署说明
1. 安装命令行工具 **Serverless Framework**
```
npm install -g serverless
```

2. 下载项目模版代码并进入模版目录
```
sls init biliexp-demo
cd biliexp-demo
```

3. 打开 config.json 文档，根据说明填入对应内容
```
{
    "cookieDatas":[
       {
           "SESSDATA": "",
           "bili_jct": "",
           "DedeUserID": ""
       }
   ],
   "email": "" ,
   "说明":"cookieDatas由浏览器获取， email 处填入您用于接受通知的邮件名"
}
```
cookieDatas 获取方式： 浏览器打开B站主页并登陆--》按F12打开开发者工具--》application--》cookies

[](https://img.serverlesscloud.cn/2020928/1601296845381-%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-09-28%2020.36.26.png)


4. 通过 `sls deploy` 完成部署，部署成功后，每日可自动触发

### 更多
项目模版默认配置每天 15:30 的定时触发，部署地域在广州，您可以通过修改 serverless.yml 配置文件，修改您的更多项目配置信息
