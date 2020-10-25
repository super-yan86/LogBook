---
weight: 1
title: "一些免费的云资源"
date: 2020-10-26T02:18:19+08:00
draft: false
author: "YC"
description: "这篇文章介绍一些免费的云资源"
resources:
- name: "featured-image"
  src: "featured-image.png"

tags: ["vps"]
categories: ["vps"]

lightgallery: true
---

```markdown
# 云

IaaS指提供系统（可以自己选）或者储存空间之类的硬件，软件要自己手动装；PaaS提供软件/框架（可以自己选）；SaaS只能使用开发好的软件（卖软件本身）；BaaS一般类似于非关系数据库，但各家不通用，有时还有一些其它东西。

## 其他人的集合

* https://github.com/ripienaar/free-for-dev
* https://github.com/AchoArnold/discount-for-student-dev
* https://github.com/qinghuaiorg/free-for-dev-zh
* https://github.com/vincenthou/free-for-china-dev
* https://github.com/ivmm/Student-resources

## 支持.net的PaaS

* https://appharbor.com 看起来比较好，支持Core 3.0
* https://www.gearhost.com/ 看起来比较好。还支持PHP7和node，即将支持Core 3.0；有10MB数据库。但硬盘只有100MB，按[教程](https://www.gearhost.com/documentation/deploy-net-core-application)说的自包含的貌似已经超了
* https://www.aspify.com/en/webhosting/aspnet-freehosting/ 100MB硬盘100MB数据库，支持Core
* https://freeasphosting.net/ 看起来不怎么样，虽然写了免费，但是整个网站都在说学习
* https://somee.com/ 被墙了，且IP被封了

## 不支持.net的PaaS

* https://www.heroku.com/ 不过支持docker，相当于支持所有语言
* https://www.pythonanywhere.com/ 限制非常多，几乎就和虚拟主机差不多了，免费账户不允许访问白名单之外的网站。但好歹能提供一个自动https的web app
* https://cloud.google.com/appengine/docs/ 标准环境有一点储存空间和流量，柔性环境必须启用结算；然而.NET只有柔性环境，且现在标准环境要启用一个API，而这个API要求绑卡
* https://www.cloud66.com/node/ 免费一个月
* https://coded.sh/ Node；现在挂了
* https://www.engineyard.com/ ruby node php
* https://runkit.com Node
* https://fly.io/docs/pricing/
* https://nexusbytes.com/cart.php?gid=1 python和nodejs
* https://m3o.com/ Go，但是现在是invite only
* https://anvil.works/ Python
* https://www.openode.io/pricing node
* https://glitch.com node

## 云端空间/IDE？

* https://www.tutorialspoint.com/codingground.htm http://codepad.org/ https://ideone.com/ https://coliru.stacked-crooked.com/  ：无需登录，能执行许多语言，但只能说能运行代码，根本称不上IDE
* https://studio.dev.tencent.com/ 有shell，有IDE（魔改VSC，不太好用）；有个一键发布可以在公网上访问到但只支持静态页面和PHP，有128M MySQL但只能在内网访问到。运行.NET只能创建一个每次限时一小时的链接，且是Core 2.1。现在变成 https://cloudstudio.net 了，是原版VSC，没有一键部署了，能生成有外部链接的预览，服务器在上海，但每个用户每日只能使用工作空间共两小时；没有预装.NET Core，但居然能完整装下，硬盘空间还是蛮多的，有50G
* https://che.openshift.io/dashboard/ 之前是codenvy；现在是在线VSC，速度和完成度都还不错，但不支持扩展
* https://www.gitpod.io/ 有免费版；专业版在学生包里免费6个月
* https://colab.research.google.com/ 在线jupyter notebook，宣传说有免费gpu额度，国内无法直接打开
* https://aistudio.baidu.com
* https://vitu.ai 现在用不了
* https://code.xueersi.com/ide/code/1 只有C++，很简陋
* https://tianchi.aliyun.com/notebook-ai/home jupyter lab，有免费gpu，能连续运行8小时，5G空间
* https://www.kaggle.com notebook，验证电话后有免费gpu和外网，能连续运行9小时，有编程教程
* https://repl.it/ 有免费版；专业版在学生包里免费3个月

### 前端在线IDE

* https://codepen.io/
* https://stackblitz.com/
* https://jsfiddle.net/ 我这里打开非常慢
* https://codesandbox.io/
* https://trinket.io/
* https://bit.dev/

## 免费数据库

* https://db4free.net/ ：mysql 不超过200M
* https://www.freemysqlhosting.net/ ：mysql，5MB
* https://mlab.com/ mongodb，500MB
* https://app.redislabs.com/ redis，30M

## BaaS

* https://bmob.cn/
* https://leancloud.cn/pricing/
* https://www.freesqldatabase.com/
* https://firebase.google.cn/pricing 用处：https://zhuanlan.zhihu.com/p/95334890
* https://www.zhihu.com/question/34124789/answer/72495188
* https://maxleap.cn/s/web/zh_cn/devcenter-pricing.html
* https://www.back4app.com/
* https://hasura.io/

## 也许可用的IaaS

* https://www.litespeedtech.com/experience-litespeed-for-free 一个月有效？需要姓名，电话，邮箱，地址
* https://open.iot.10086.cn/cloud/introduction/cloud-server OneNET移动的，MQ、对象储存、可视化、CI都有一定的免费额度
* https://cloud.tencent.com/act/free 腾讯云，个人验证后有一些可以长期免费使用；现在容器内测，本身是免费的，其它服务收费；云函数公测暂时免费
* https://activity.xinruiyun.cn/free/ 新睿云，发个广告可以免费用一个月的ECS
* https://www.oracle.com/cn/cloud/free/ 体验文章：https://51.ruyo.net/14138.html
* https://51.ruyo.net/14583.html Azure
* https://51.ruyo.net/12065.html https://www.ibm.com/cn-zh/cloud/free IBM，Lite版无需信用卡
* https://www.clever-cloud.com/en/pricing
* https://www.atlantic.net/ 免费12个月，需要信用卡
* euserv，德国的，只有IPV6

## Free Managed K8S

* https://okteto.com/pricing 免费版2CPU，4G内存，10G储存。刚注册送一个月pro，不付款自动降到免费版。免费版24小时不活动就sleep。原意是为开发者日常开发使用的
* https://www.openshift.com/products/online/ 每60天清除
* https://usekrucible.com 一个月能用25小时，自己分配
* https://kubesail.com/ 必须用GitHub，有WebUI，1vCPU，1G内存，100M储存；10月停止免费版了，不过还是支持添加自己的服务器
* https://kubernauts.sh/ 免费版有1CPU，1G内存；注册了但什么邮件也没收到，也没有登录的地方
* https://tryk8s.com/ ~~必须用GitHub，好像直接就是免费的，但是明说了24小时后回收所有资源~~好像是国产的，且是阿里云相关的，且现在已经挂了
* https://labs.play-with-k8s.com/ 好像每天只有四小时；https://labs.play-with-docker.com/
* https://k8spin.cloud/ 必须用GitHub或Google账户登录。8月后转变为管理平台
* zarvis.ai staroid.com 网页都用的是Google的服务器，无法直接访问
* https://devspace.cloud/ 好像只是客户端或者管理平台

## Serverless

* https://glitch.com/
* https://workers.cloudflare.com/
* https://zeit.co https://vercel.com/
* https://pipedream.com/
* https://keen.io/

## 低代码平台/aPaaS/SaaS

指不用写很多代码就能设计出软件，有可视化工具。
“所谓的快速开发平台在我看来已经是一种陈旧的观念, 其最大的问题是认为员工是廉价，工业化的。在持有这种观念的企业中，个人无法获得提升，无法发挥人这个重要的促进因素，在一个条条框框中工作，工作没有任何激情，长期以往，企业也是没有核心竞争力的。因为它忽略了人是个性化，需要自身发展这个重要因素。轻开发平台，重库重用，重最佳实践，最佳实践可以随时调整，而开发平台，转头太难。”

* https://www.outsystems.com/pricing-and-editions/ 开发移动应用，是该行的老大；前端组件比较多，后台相对弱一点儿；注册需要姓名，邮箱
* https://www.mendix.com/ 开发移动应用，后台能力比较强（有微流系统）
* https://www.kony.com/
* https://free.caspio.com/ Create Database-Powered Apps
* https://thunkable.com 开发移动应用
* https://www.appsheet.com/
* https://www.zoho.com/creator/ 网页在我这里打开巨慢。可以stay in the Free Plan只要不使用premium features
* https://airtable.com/
* https://zenkit.com/
* Google的App Maker（G Suite收费）、微软的PowerApps（收费10$/mo）
* https://www.odoo.com/zh_CN/

国内的：

* https://www.aliwork.com/ 宜搭，阿里云的，有完全免费的版本
* https://www.apicloud.com/ 有免费版
* https://www.mingdao.com/ 明道云。没说有免费版
* https://h3yun.com/ 氚云，没说有免费版 https://www.cloudpivot.cn/ 云枢 https://www.h3bpm.com/ 都是“奥哲”公司的
* https://www.newdao.net/ 牛刀，没说有免费版
* https://www.jiandaoyun.com/ 简道云，有免费版
* https://www.huoban.com/ 伙伴云，没说有免费版
* https://qingflow.com/ 轻流，有免费版
* https://www.steedos.com/platform/pricing/
* https://aipage.baidu.com/ https://baidu.gitee.io/amis/docs/index
* ---
* https://www.iyunbiao.com/ 云表，可以用来实现xxx管理系统
* https://www.grapecity.com.cn/solutions/huozige 活字格
* https://enhancer.io/ 无远开发平台
* https://www.learun.cn/ 力软敏捷框架
* https://www.ih5.cn 后来出了 https://www.ivx.cn 但前者貌似也还活着。是个零代码开发平台，只能开发Web App和小程序
* https://www.wudaima.com/ 宜创无代码，收费
* https://wuyuan.io/ 无远开发平台，个人使用免费，商业收费
* 没有https的：http://www.bossietech.com/ 柏思科技/Workfine 、http://www.joget.cn/ 捷得 、http://www.putdb.com/ WebBuilder 、http://www.mf999.com/ 魔方网表、http://www.delit.cn/ 度量快速开发平台、http://www.jinyunweb.com 进云、Http://dev.easydo.cn 易开发、www.clickpaas.com

## 未分类

* https://help.aliyun.com/document_detail/54301.html#Free FaaS 有一点免费额度
* https://github-students.educationhost.co.uk/ 好像只有静态网页，但是很靠谱；只有一年

## 自己搭建的

集合：https://paasfinder.org

* http://dokku.viewdocs.io/dokku/
* openstack，开源IaaS，机器最好有10G以上的内存
* rancher, openshift, CloudFoundry和Flynn也可以自己搭建，是PaaS
* https://www.rainbond.com/ 国产的
* https://letscoded.com
* https://www.koding.com/
* https://kodcloud.com/
* https://github.com/caprover/caprover
* https://convox.com/
* https://nanobox.io/
* https://caprover.com/
* https://rio.io/

```


