# springboot-shiro-cas-mybatis
参考来源-https://github.com/zzuhub/sso-client-rep.git    【cas-shiro-redis-mybatis-springboot】

这个是一个springboot工程

配置了Windows  C:\Windows\System32\drivers\etc\hosts下面
127.0.0.1 www.cas.com   模拟cas认证中心
127.0.0.1 www.ssoclient.com   cas客户端

blog是一些网上参考的博客

cas-4.1.0是sso认证服务端的官方代码

sso-client-rep-master是客户端shiro-cas(1.2.4)的代码-使用了Redis作为shiro的缓存


testredisshiro.sql是数据库代码-mysql


controller是一些测试获取信息

RestController.java是模拟rest登录获取tgt和st





说明：
1.目前是前后端代码一个工程传统的单体（javaweb jsp 或者 freemaker形式）；
###################################################################################################################
2.测试了一下如果前后端分离通过rest接口调用，但是也把前端代码放在一个工程应该没问题（比如放在static目录）；
但是但是！！！
###################################################################################################################
3.但是前后端彻底分开部署，不在一起
（将来springboot微服务下，多个模块，前端直接放在NGINX上面，后端每个微服务一台机器，前端ajax调用rest后端接口，用流行的angular vue  react等），
  参考了大神的思路（http://blog.csdn.net/a7695895/article/details/53262494），获取tgt，在获取st，但是没有成功，获取了st接待着st访问一个接口还是被重定向到
  认证中心登录了。------应该是我自己没理解到位或者配置出错。
  ###################################################################################################################
4.加上APP端（原生挥着h5开发登录页面必须在手机本地不会重定向到认证中心）------感觉应该照按照大神的思路（http://blog.csdn.net/a7695895/article/details/53262494），
的思路获得st访问应该没有问题，但是我自己没弄成功。
