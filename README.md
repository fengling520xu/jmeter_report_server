# JMeter Report

![](https://img.shields.io/badge/JMeter-green)
[![](https://img.shields.io/github/last-commit/hui-huo/jmeter_report_server)](https://github.com/hui-huo/jmeter_report_server)

基于Antd+DRF开发的一款JMeter测试报告服务，用于在JMeter接口测试中使用。
**[效果体验](http://1.116.137.209:8000/dashboard)**

## 🌴 背景

JMeter是测试工作中常用的一款工具，除了压测还可以用来做接口自动化的测试。

从事测试多年，接口自动化也做过很多的尝试，有时候所在项目迭代较快，平常没有足够的时间 编写自动化测试脚本，但又想在日常测试中加入自动化来提高点效率，JMeter是一个不错的选择。
缺点就是官方没有提高好的测试报告（相信很多人都是颜值控😂），于是就有了这款适配JMeter的测试报告。

虽然功能比较简单，但已满足基本日常需求。

## 0610更新

- 新增：测试场景数量统计
- 新增：测试报告页删除功能
- 优化：测试用例展示

## 实现

<img src="https://files.mdnice.com/user/25329/8ff683b1-4e1f-4a52-b131-24b8564d6d57.png" alt="实现原理" width="800" height="500" />

## 📌 安装和使用

### 1. docker启动服务

1. `docker pull huihuo21/jmeter-report`
2. `docker run -d -p 8000:8000 huihuo21/jmeter-report`
3. 浏览器访问`http://{服务ip}:8000`

默认启动使用内置`sqlite`，若指定数据库(仅支持`mysql`)则需要传入参数（生产使用建议使用此方式）

HOST和PORT可选，默认`localhost`, `3306`

```
docker run -d -p 8000:8000 \
-e DB_NAME=数据库名称 \
-e DB_USER=用户名 \
-e DB_PASSWORD=密码 \
-e DB_HOST=IP \ 
-e DB_PORT=端口 \
huihuo21/jmeter-report
```

### 2. 安装JMeter插件

JMeter 后置监听器插件：用于测试数据的收集 [JMeter-Backend-Listener](https://github.com/hui-huo/JMeter-Backend-Listener)


## 🔎 页面预览

### 测试看板

![dashboard](https://files.mdnice.com/user/25329/259dd04c-1906-405f-bf7e-ed55efa2cd22.png)

### 测试详情

![detail](https://files.mdnice.com/user/25329/16221abb-9141-4801-80ec-2461dbd90d3f.png)


## 交流群

二维码会经常过期，可以加我个人微信: *`_huihuo`*，拉你入群。

<img src="https://files.mdnice.com/user/25329/510e20fe-2c77-4b5f-b05d-c36332551a7f.png" alt="_huihuo" width="300" height="300" />




