# Small



![](https://github.com/mn3711698/Small/blob/master/923.png)

#### 注意：用docker镜像mn3711698/small:004的一定要git pull，这个镜像我不会再更新代码，需要自己git pull,不然代码会很旧，没法用!


## 请务必使用python3.6  请务必使用python3.6  请务必使用python3.6

## 说明  2019-08-07
docker镜像基于ubuntu 18.04 的python3.6.8+postgresql-10,数据库要开下pgcrypto。命令是：create extension pgcrypto;
<br>mn3711698/small:004,我测试过OK。
<br>您完全可以直接在里边的/var/games/Small下，安装(python3 install.py)及运行(python3 start.py)。
<br>以后docker里的代码我就不更新了，有需要的直接git pull就好了。
<br>我是将整个环境都弄好打包成一个，直接在docker里边运行，我也不懂别的方法，这样有个问题就是，那个安装生成的dbconfig.py文件没有，每次都要重新搞。
<br>python3 start.py启动项目通常是用来调试的，如果要生产运行，您可以用nginx+apache或者别的方法，我是用nginx+apache。

本系统采用python3,基于flask搭建的脚手架开发。数据库是postgresql.
<br>请注意config.py这个配置文件，默认开启调试日志。

配合SmallStore开源小程序使用：https://github.com/mn3711698/SmallStore


models里的模型已处理好。
docker已处理好。


最终将会是一个进销存ERP，供销等功能及接口（小程序，微信公众号，H5，APP）的平台。
<br>提供私有化部署，共享部署，接口等。

> 
> 

目前功能是比较少，将会不断增加，同时也期待您贡献代码或者功能。


## 功能特性
> - [x] 表示已开发
> - [ ] 表示准备开发


- [x] 小程序管理
    * 店铺设置
        * OSS存储设置
        * 店铺信息设置
        * 商铺设置
        * 订单设置
        * 小程序设置
        * 会员设置
        * 全局设置
        * 积分规则设置
        * 充值设置
        * 快递鸟设置
    * 图片广告
    * 文字广告
    * 文章分类
    * 文章列表
    * 用户列表
    * 用户地址
    * 用户反馈
    
- [x] 商品管理
    * 商品分类
    * 商品规格
    * 商品档案
    * 商品评价
    * 商品热销榜
    * 商品反馈
    
- [x] 营销中心
    * 优惠券
    * 拼团活动
    
- [x] 订单管理
    * 销售订单
    * 退款订单
    * 售后订单
    
- [x] 综合查询
    * 优惠券查询
    * 充值查询
    * 返现查询
    * 消费查询
    * 会员升级查询
    * 图片查询
    
- [x] 系统管理
    * 个人帐号
    * 角色授权
    * 人员管理
    * 人员授权
    * 登录日志
    * 帐号解锁


- [ ] 公众号管理
    * 基本设置
    * 自定义菜单设置
    * 文字回复
    * 图文设置
    * 音乐设置
    * 特殊回复
    * 粉丝列表

- [ ] 帐号管理
    * 子帐号设置
    * 子帐号角色
    * 子帐号授权
    
- [ ] 平台设置
    * 收费管理
    * 商家公告
    

     
                                                                                        

## 目录模块功能

```shell
├── admin  //后台目录（比较多，还未整理）
│   ├── dl  //路由映射的数据处理
│   │
│   ├── html  //html文件
│   │
│   └── vi  //对应路由文件
│
│
│
├── api  // 小程序目录
│   ├── BASE_LOC.py
│   ├── BASE_TPL.py
│   ├── helper.py
│   ├── home.py
│   ├── pay.py
│   ├── VI_BASE.py
│   ├── VIEWS.py
│   └── wxpay.py
│
├── basic  //共用文件目录
│   ├── base.py
│   ├── pay.py
│   ├── preload.py
│   ├── publicw.so
│   ├── RE_TOOL.py
│   ├── wxbase.py
│   └── wxpublic.py
│ 
├── celery_app  // 定时任务目录
│   ├── celeryconfig.py
│   ├── db_backup.py
│   └── pfc.py
│
├── models  // 数据库表
│   └── model.py
│   
├── static  //css,js,img等静态文件
│     
│   
├── templates  //安装过程的html
│   
│   
└── wxpay  // 微信支付回调
│     └── WxPay.py   
│   
├── config.py //基本配置
├── install.py //安装启动
├── start.py //项目运行启动
└── zone.py //七牛上传修改
```

## 目前系统还在完善中，如果有bug请加下边的QQ群反馈，感谢！


# QQ群
528289471

# License
为了增加运行效率及防止出现有人将代码随意进行销售，特将部分代码采用cython处理。不会收集任何个人敏感信息，并且项目将客户存在数据库的敏感信息有加密处理，具体可以看代码。
> 在不贡献代码、功能、小程序模板的情况下，只要不是将代码直接销售获利，不禁止任何形式的使用、修改、发布、分发该软件。那怕用在公司商业使用或者自己部署平台进行服务销售也不影响，我也赞成这样的使用。

> 在贡献代码、功能、小程序模板的前提,并得到我确认下的情况下，您可以为所欲为。

* 本项目能发展得起来最终会完全开源，不会有任何代码用cython处理。初期为了可控，不进行完全开源。
