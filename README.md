# e_shop_yii2
基于Yii2+PHP7+MySQL8+Redis 的开源 单店铺 商城

## version
Yii2.0.36


<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <h1 align="center">Yii 2 Advanced Project Template</h1>
    <br>
</p>

Yii 2 Advanced Project Template is a skeleton [Yii 2](http://www.yiiframework.com/) application best for
developing complex Web applications with multiple tiers.

The template includes three tiers: front end, back end, and console, each of which
is a separate Yii application.

The template is designed to work in a team development environment. It supports
deploying the application in different environments.

Documentation is at [docs/guide/README.md](docs/guide/README.md).

[![Latest Stable Version](https://img.shields.io/packagist/v/yiisoft/yii2-app-advanced.svg)](https://packagist.org/packages/yiisoft/yii2-app-advanced)
[![Total Downloads](https://img.shields.io/packagist/dt/yiisoft/yii2-app-advanced.svg)](https://packagist.org/packages/yiisoft/yii2-app-advanced)
[![Build Status](https://travis-ci.com/yiisoft/yii2-app-advanced.svg?branch=master)](https://travis-ci.com/yiisoft/yii2-app-advanced)

DIRECTORY STRUCTURE
-------------------
    [M] Model       模型层  映射数据表，校验数据，加工数据
    [V] View        视图层  页面模板
    [C] Controller  调度层  调用Service、渲染View
    [S] Service     服务层  调用Model 实现业务逻辑

    [T] Test        测试
    [L] Log         日志
```
common
    base/                基类，扩展Yii2自身提供的基类
    config/              全局配置项 区分环境的 *-local.php 应配置在environments目录下，通过 php init 指定环境
    mail/                [V]共用的邮件模板
    models/              [M]共用的ActiveRecord、ActiveQuery、*Search
    tests/               [T]自动化测试   
console
    config/              当前模块配置
    controllers/         可在命令行执行的脚本，没有登录态
    migrations/          数据库迁移文件，建议每个版本对应一个目录
    models/              当前模块专用的model文件，建议继承 common/models下的文件
    runtime/             通过当前应用执行的程序，产生的运行时文件
api                 通用接口    
    config/              当前模块配置
    controllers/         [C]
    models/              [M]当前模块专用的model文件，建议继承 common/models下的文件
    runtime/             [L]通过当前应用执行的程序，产生的运行时文件
    tests/               [T]自动化测试
    services/            [S]业务逻辑，调用[M] 
    forms                [M]表单，校验数据，建议一个场景使用一个表单，不指定场景
backend             后台管理(运维、开关配置、权限管理、操作日志)
    assets/              前端资源JavaScript、CSS
    config/              当前模块配置
    controllers/         [C]
    forms                [M]表单，校验数据，建议一个场景使用一个表单，不指定场景
    models/              [M]当前模块专用的model文件，建议继承 common/models下的文件
    runtime/             [L]通过当前应用执行的程序，产生的运行时文件
    services/            [S]业务逻辑，调用[M] 
    tests/               [T]自动化测试     
    views/               [V]页面模板
    web/                 入口脚本、web资源
frontend            WEB站点
    assets/              前端资源JavaScript、CSS
    config/              当前模块配置
    controllers/         [C]
    forms                [M]表单，校验数据，建议一个场景使用一个表单，不指定场景
    models/              [M]当前模块专用的model文件，建议继承 common/models下的文件
    runtime/             [L]通过当前应用执行的程序，产生的运行时文件
    services/            [S]业务逻辑，调用[M] 
    tests/               [T]自动化测试 
    views/               [V]页面模板
    web/                 入口脚本、web资源
    widgets/             [V]视图挂件
vendor/                  第三方包，建议过滤在版本库之外
environments/            区分环境(prod、dev、test)配置数据
```
