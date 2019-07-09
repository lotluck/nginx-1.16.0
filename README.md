
nginx-1.16.0
====
nginx-1.16.0源码分析及其注释--记录心路历程
----

## [一. myexercise--练习调试一些nginx的代码](https://github.com/lotluck/nginx-1.16.0/tree/master/myexercise)<br>
### [1.myngx_pool.c](https://github.com/lotluck/nginx-1.16.0/tree/master/myexercise/myngx_pool)<br>
>> #### 调试练习ngx_pool.c的代码

### [2.myngx_hash](https://github.com/lotluck/nginx-1.16.0/tree/master/myexercise/myngx_hash)<br>
>> #### 调试练习ngx_hash.c的代码


## [二.mymodule--自己编写一些模块](https://github.com/lotluck/nginx-1.16.0/tree/master/mymodule)<br>
### 1.ngx_http_myhello_module<br>
>> #### 自己编写的一些hello模块，用来熟悉和掌握nginx
>> #### ./configure --prefix=/data4/nginx/nginx --add-module=./third-module/tmp/echo-nginx-module-0.61 --with-debug --add-module=./mymodule/ngx_http_myhello_module/  && make -j8 && make install


## 三.已翻译代码
### 1.HTTP模块<br>
>> #### a) HTTP的11个阶段入口   src/http/ngx_http_core_module.c -- 特别重要
>> #### b) 待添加  
 
### 2.配置相关<br>
>> #### a) 模块上下文结构体   --- 待完成
>> #### b) 模块结构体   --待完成
>> #### c) ngx_command_t 配置指令结构体 -- 待完成

### 3.数据结构<br>
>> #### a) ngx_pool_t 内存池--src/core/ngx_palloc.c、src/os/unix/ngx_alloc.c 
>> #### b) ngx_hash_elt_t  nginx哈希表 -- src/core/ngx_hash.c
>> #### c) ngx_array_t    动态数组 -- src/core/ngx_array.c
>> #### d) ngx_list_t  链表 --  src/core/ngx_list.c


## [四.third-module -- 第三方模块](https://github.com/lotluck/nginx-1.16.0/tree/master/third-module)<br>
### 1.echo-nginx-module<br>
>> ####  [echo-nginx-module原地址](https://github.com/openresty/echo-nginx-module)<br>
>> ####  nginx.conf中通过echo等指令直接输出包体， 类似于nginx的命令，方便调试配置
>> ####  ./configure --prefix=/data4/nginx/nginx --add-module=./third-module/echo-nginx-module-0.61 && make -j8 && make install


## [五.books -- 相关书籍](https://github.com/lotluck/nginx-1.16.0/tree/master/books)<br>
### 1. nginx
>> #### a) 《深入理解nginx》--陶辉
>> #### b) 《深入剖析nginx》

### 2. http
>> #### a) 《图解HTTP》
>> #### b) 《图解TCP/IP》



## [六.tools -- 相关工具](https://github.com/lotluck/nginx-1.16.0/tree/master/tools)
### 1. ab 压测工具
>> #### yum install httpd-tools
>> #### 直接上手ab -n 1000 -c 5 http://1.1.1.1/1.mp4
### 2. stress
>> #### 待添加




