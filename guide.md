## 由html文件生成pdf文档的方法说明 ##

<h3>环境准备</h3>

安装wkhtmltopdf工具
下载地址：[http://code.google.com/p/wkhtmltopdf/downloads/list
](http://code.google.com/p/wkhtmltopdf/downloads/list)

把wkhtmltopdf工具的后的文件添加到系统的path环境变量中

下载安装Adobe Acrobat X Pro工具
下载地址：[http://www.xiazaiba.com/html/5263.html](http://www.xiazaiba.com/html/5263.html)

<h3>生成步骤</h3>

- 首先通过sphinx工具导出html格式的文档(请参照其他文档)

- 把sphinx生成的文档放到应用容器下，如tomcat（这一步为了支持图片，否则图片可能不能正常显示）

- 在windows控制台中运行如下脚本（需要工具你的机器修改相应的参数）：

    wkhtmltopdf http://192.168.0.104:8080/api/api-overview.html 
    overview.pdf --outline

note:第一个参数为待转换的html文件路径，第二个参数为生成的pdf文档的文件名，第三个参数指定生成pdf文档的书签

- 最后使用Adobe Acrobat X Pro工具的	`将文件合并为pdf`的功能对多文件进行合并编辑


