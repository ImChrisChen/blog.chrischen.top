---
title: 如何进行Web程序性能优化🛁

date: 2019-08-17 13:27:10

categories:
  - 性能优化

tags: 
  - html
  - css
  - Javascript
---



## 浏览器

### html

- 减少DOM数量

- 不要在HTML中拉伸图片 （会重新绘制）

  

### css

- 避免重复定义CSS，CSS覆盖等
- 不使用CSS表达式



### javascript

- 减少DOM访问（避免重绘 和 回流）
- 合理设计事件监听器
- 避免 DOM 阻塞 （JavaScript放在最后面，或者加上defer 标签）



## 资源

- 静态资源压缩，使用CDN



## 缓存

- 客户端缓存
- 服务端缓存
- http 缓存



## 网络Http

- 减少 HTTP 请求数量（合并文件、CSS精灵 (图片合成)、inline Image）
- 减少 HTTP 请求大小
- 添加Expires或者Cache-Control响应头



## 服务器

- nginx 开启 gzip 压缩
- 减小cookie大小
- 引入资源的域名不要包含cookie
- 

### content方面

-   减少HTTP请求：合并文件、CSS精灵 (图片合成)、inline Image
-   减少DNS查询：DNS查询完成之前浏览器不能从这个主机下载任何任何文件。方法：DNS缓存、将资源分布到恰当数量的主机名，平衡并行下载和DNS查询
-   避免重定向：多余的中间访问
-   使Ajax可缓存
-   非必须组件延迟加载 ( 插件，组件，图片等懒加载同理 )
-   未来所需组件预加载
-   减少DOM元素数量
-   将资源放到不同的域下：浏览器同时从一个域下载资源的数目有限，增加域可以提高并行下载量
-   减少iframe数量
-   避免404



### Server方面

-   使用CDN
-   
-   配置ETag
-   Flush Buffer Early
-   Ajax使用GET进行请求