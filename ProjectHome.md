一个生成真实服务器位置、状态、一般信息模拟图。<br>
效果展示：<a href='http://blog.liuts.com/idc/'><a href='http://blog.liuts.com/idc/'>http://blog.liuts.com/idc/</a></a>

<h2>一、开发包</h2>
<ul><li>c++<br>
</li><li>CMake</li></ul>

<h3>二、系统截图</h3>
<ol><li>平台显示某一排截图<br>
</li></ol><blockquote><img src='http://blog.liuts.com/attachment/201007/1278641825_3347e6a7.png' width='800'><br><br>
2.平台显示某台服务器详细信息截图<br>
<img src='http://blog.liuts.com/attachment/201007/1278641825_48837306.png' width='800'><br><br>
3.状态说明<br>
<blockquote>2U服务器正常状态<br>
<img src='http://blog.liuts.com/attachment/201007/1278641825_7986e83a.gif'><br><br>
2U服务器当机状态<br>
<img src='http://blog.liuts.com/attachment/201007/1278641825_665978e3.gif'><br></blockquote></blockquote>

<h3>三、系统原理</h3>
<blockquote>通过获取运维平台的服务器信息(包括位置、操作系统、机型等)，格式为XML，通过c++的tinyxml来解析并渲染成比较美观的HTML格式。当机的信息通过Nagios来获取。这样就可以生成非常人性化的展现平台了：）</blockquote>

<h3>四、常见问题</h3>
1、运行#./servermap提示：<br>
Segmentation fault<br>
<br>
原因：<br>
由于servermap是在默认配置的路径进行编译，在解压ServerMap1.0.1.tar.gz包后请确认当前路径是否与默认一致；<br>
<br>最终解压后的默认路径为：/home/ServerMap/<br>
<br>
<br><br>确认输出HTML文件位置的路径是否存在，不存在则手工创建；<br>
<br>/home/webroot/<br>
<br>
<b>当然也可以修改servermap.cpp的相关路径后再编译，建议使用cmake。<br>
<hr />
<hr /></b>

BLOG：<a href='http://blog.liuts.com'><a href='http://blog.liuts.com'>http://blog.liuts.com</a></a><br>
微博：<a href='http://t.qq.com/yorkoliu'><a href='http://t.qq.com/yorkoliu'>http://t.qq.com/yorkoliu</a></a><br>
交流QQ群：158926355