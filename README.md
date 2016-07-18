# 慕课网实战课程-- 手机阅读器 webapp

以下是每天在学习实战课程中所遇到的一些琐碎的知识点,在视频中不能立刻理解的地方

## 日记1 14/7
### reset.css 的作用
[百度百科链接](http://baike.baidu.com/view/5186496.htm)

由于浏览器在加载html时,会对html加载默认的样式,如`p`的上下编辑,`strong`的加粗,`ul`的缩进等,这就为我们在开发的过程中带来困扰,所以需要通过reset.css来重新定义标签样式,同时也使得不同浏览器中的显示样式得到统一


### base64 图片的作用
其最大的作用就是进行性能优化,相较于以前的img中加上图片地址,这种方法减少了网络请求,避免了跨域请求和图片缓存的问题.但换来的是css文件的大小增加

### css3 的 子元素选择器
在`index.html`中为了让ul的第二个子元素不出现右边框使用了子选择器`li:nth-child(2)`,值得注意的是css中的子元素序号是从1开始的,同时,这段也可以写成`li:last-child` 以匹配最后一个子元素.

## 日记2 15/7
### 顶部/底部 固定菜单栏
1.  将菜单栏的最外层的`position` 设为fixed 即相对于浏览器窗口不变,并设置高度
2.  将其中的元素,如返回按钮与标题的 `position`设为`absolute` 并根据设计图调整其相对夫元素的位置

### ase64
1.  Base64格式
  `data:[][;charset=][;base64]`
2.  Base64 在CSS中的使用
  `.demoImg{ background-image: url("data:image/jpg;base64,/9j/4QMZRXhpZgAASUkqAAgAAAAL...."); }`
3.  Base64 在HTML中的使用
  `<img width="40" height="30" src="data:image/jpg;base64,/9j/4QMZRXhpZgAASUkqAAgAAAAL...." />`
4.  png图片转化为base64 可以使用[在线网站](http://tool.css-js.com/base64.html)
