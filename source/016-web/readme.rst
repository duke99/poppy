web
###

.. toctree::
   :maxdepth: 2

   001-nginx/readme
   002-httpd/readme
   003-tomcat/readme



访问http时response对象返回值
=======================================



状态码	说明	状态码	  说明
100	继续	    404	    资源未找到
101	转换协议	405	    方式不被允许
200	OK，成功	406	    不接受的
201	已创建	    407	    需要代理验证
202	接受	    408	    请求超时
203	非权威消息	409	    冲突
204	无内容	    410	    不存在
205	重置内容	411	    长度必需
206	部分内容	412	    先决条件失败
300	多个选择	413	    请求实体太长
301	永久移动	414	    请求URI太大
302	发现	    415	    不被支持的媒体类型
303	见其它	    500	    服务器内部错误
304	没有被改变	501	    不能实现
305	使用代理	502	    坏网关
400	坏请求	    503	    服务不能获得
401	未授权的	504	    网关超时
402	必要的支付	505	    HTTP版本不支持
403	禁用
