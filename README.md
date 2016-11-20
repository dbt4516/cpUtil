# 去除QQ为URL自动添加的安全标识
## 1 现实痛点
如果聊天内容包含URL，复制到word中十分难看，而且去掉这些图标得手动删除。<br>
![](https://github.com/dbt4516/cpUtil/blob/master/raw/cbUtil1.png)<br>
## 2 实现思路
监听剪贴板，将小图标替换掉。<br>
据上午的观察，QQ在将数据写入剪贴板时会连带写入一种QQ_RichEdit_Format类型，可用这种类型来指示数据是否从QQ处得来，做针对处理。下午在和老大一起测试时，发现某些情况下，可能不会写入QQ_RichEdit_Format类型，所以只能改成全量处理。另外，读取剪贴板时需要做UTF8编码转换，否则可能出现汉字乱码，影响临时图片文件的显示。
## 3 效果
目前效果如下：<br>
![](https://github.com/dbt4516/cpUtil/blob/master/raw/cbUtil2.png)<br>
## 4 附加
之前发布的TsUtil在公司的电脑上经常出现已经加入自启动菜单但又时不时莫名被删除的情况，目前从手动添加至启动目录改成启动时写注册表，希望能有用。<br>
<br>
hongzhan<br>
2016-11-20<br>
