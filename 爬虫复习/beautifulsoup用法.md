```
from bs4 import BeautifulSoup
soup = BeautifulSoup("<html><head><title>爬虫教程</title></head><body><p>爬虫教程</p></body></html>", "html.parser")
soup2 = BeautifulSoup(open("D://demo.html"), "html.parser") # lxml文件 html5lib文件
print(soup.prettify()) # 格式化输出
print(soup.title) # 获取title标签
tag = soup.a # 获取a标签
print(tag) # 获取a标签内容
print(tag.attrs) # 获取a标签属性
print(tag.attrs['class']) # 获取class标签内容
print(soup.name) # 获取标签名称

# 1. BeautifulSoup对象的创建
html = """
<html>
<head><title>My Title</title></head>
<body>
<p class="story">Once upon a time...</p>
<div id="content">
    <p>This is some text.</p>
</div>
</body>
</html>
"""
soup = BeautifulSoup(html, 'html.parser') # 'html.parser' 是内置解析器
# 2. BeautifulSoup对象的基本操作
title_tag = soup.find('title') # 查找 <title> 标签
p_tags = soup.find_all('p') # 查找所有 <p> 标签
story_tag = soup.find('p', class_='story') # 查找 class 为 'story' 的 <p> 标签
content_div = soup.find(id='content') # 查找 id 为 'content' 的元素
# 3. 提取相关的内容
title_text = title_tag.text # 获取 <title> 标签的文本内容
story_text = story_tag.text # 获取 class 为 'story' 的 <p> 标签的文本内容
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwODMxNDExNzVdfQ==
-->