```
# requests.get("https://www.baidu.com/s", params = kv, **kwargs) 从指定的 URL 检索（获取）资源。
# requests.post(url, data=None, json=None, **kwargs)向指定的URL发送数据，处理数据输入的操作
# requests.put(url, data=None, **kwargs)向指定的URL发送数据，处理数据更新的操作
# requests.delete(url, **kwargs)向指定的URL发送数据，处理数据删除的操作
# requests.head(url, **kwargs)向指定的URL发送数据，处理数据头部的操作
# requests.options(url, **kwargs)向指定的URL发送数据，处理数据选项的操作
# requests.patch(url, data=None, **kwargs)向指定的URL发送数据，处理数据局部更新的操作
# requests.request(method, url, **kwargs)向指定的URL发送数据，处理数据请求的操作

scrapy startproject <name>
cd spiders 
scrapy genspider demo spiders.io
编辑demo文件下的url地址和解析 name start_urls解析 更改parse方法
scrapy crawl demo

# scrapy常用指令 
startproject 创建一个新的工程 scrapy startproject demo
genspider 创建一个新的爬虫 scrapy genspider demo spiders.io 
crawl 启动爬虫 scrapy crawl demo
list 列出所有爬虫 scrapy list
check 检查爬虫是否正常 scrapy check demo 
settings 显示当前爬虫的设置 scrapy list
shell 进入scrapy shell  scrapy shell https://www.baidu.com

#  < --  scrapy操作代码实战  -- > 
1. 配置爬虫文件
scrapy startproject BaiduStocks 
cd BaiduStocks
scrapy genspider stocks baidu.com 
# 编辑stocks.py文件的url地址和解析 name start_urls解析 更改parse方法

2. 开始爬虫
配置stocks.py文件的url地址和解析 name start_urls解析 更改parse方法
修改返回页面的处理
修改对新增URL爬取请求的处理

3.编写Pipelines 
配置pipelines.py文件
定义对爬取项(Scraped Item)的处理类 : 更改pipelines.py中的方法
修改ITEM_PIPELINES配置项 : 更改settings.py文件中的ITEM_PIPELINES配置项

settings文件 : 
1. concurrent_requests 最大并发请求下载数量，默认32
2. concurrent_requests_per_domain 每个域名最大并发请求数量，默认16
3. concurrent_requests_per_ip 每个IP最大并发请求数量，默认16
4. download_itemsx item pipeline最大并发item数量，默认100
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbODI4MDA1ODkwXX0=
-->