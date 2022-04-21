---
title: 解决无法访问 Github
top: true
cover: false
toc: true
mathjax: true
date: 2022-04-19 16:07:38
password:
summary: 搭建博客记录笔记
tags:
- Github
- Hexo
- 博客搭建
categories:
- Blog
---
<![CDATA[ <!-- wp:paragraph --> <p>查阅了一些资料，发现需要在hosts文件中添加映射。<br>在hosts文件中加入两行</p> <!-- /wp:paragraph --> <!-- wp:image {"id":118,"sizeSlug":"large","linkDestination":"media"} --> <figure class="wp-block-image size-large"><a href="https://imjoez.files.wordpress.com/2022/04/1.png"><img src="https://imjoez.files.wordpress.com/2022/04/1.png?w=486" alt="" class="wp-image-118" /></a></figure> <!-- /wp:image --> <!-- wp:paragraph --> <p>140.82.113.4 github.com<br>140.82.113.4 www.github.com</p> <!-- /wp:paragraph --> <!-- wp:paragraph --> <p>其中的ip地址是在&nbsp;<a href="https://github.com.ipaddress.com/www.github.com" target="_blank" rel="noreferrer noopener">https://github.com.ipaddress.com/www.github.com</a>&nbsp;中查询的</p> <!-- /wp:paragraph --> <!-- wp:image {"id":119,"sizeSlug":"large","linkDestination":"media"} --> <figure class="wp-block-image size-large"><a href="https://imjoez.files.wordpress.com/2022/04/2.png"><img src="https://imjoez.files.wordpress.com/2022/04/2.png?w=1000" alt="" class="wp-image-119" /></a></figure> <!-- /wp:image --> <!-- wp:paragraph --> <p>看很多博客介绍此时应该就可以正常访问了，但我还是无法访问，发现可能是安全证书的问题</p> <!-- /wp:paragraph --> <!-- wp:paragraph --> <p>打开 <a href="http://tool.chinaz.com/dns" target="_blank" rel="noreferrer noopener">http://tool.chinaz.com/dns</a><br>查询 github.global.ssl.fastly.net 和 assets-cdn.github.com 两个地址， 选取TTL值低的ip地址<br>把这两行写入hosts文件</p> <!-- /wp:paragraph --> <!-- wp:paragraph --> <p>清理dns缓存，win+r，输入‘cmd’，再输入ipconfig/flushdns；</p> <!-- /wp:paragraph --> <!-- wp:paragraph --> <p>就可以正常访问了</p> <!-- /wp:paragraph --> <!-- wp:image {"id":121,"sizeSlug":"large","linkDestination":"media"} --> <figure class="wp-block-image size-large"><a href="https://imjoez.files.wordpress.com/2022/04/3.png"><img src="https://imjoez.files.wordpress.com/2022/04/3.png?w=690" alt="" class="wp-image-121" /></a></figure> <!-- /wp:image --> <!-- wp:paragraph --> <p>69.171.224.40 github.global.ssl.fastly.net<br>185.199.111.153 assets-cdn.github.com<br>140.82.113.4 github.com<br>140.82.113.4 www.github.com</p> <!-- /wp:paragraph --> ]]>
