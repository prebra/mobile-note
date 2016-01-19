#移动端开发笔记
*参考 [http://www.nihaoshijie.com.cn/index.php/archives/455](http://www.nihaoshijie.com.cn/index.php/archives/455)

### 1、Meta标签
    <meta content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0;"name="viewport"/>
    <meta content="telephone=no"name="format-detection"/>  
    <meta content="email=no"name="format-detection"/>

### 2、获取滚动条的值
    window.scrollY  window.scrollX

### 3、禁止选择文本
     -webkit-user-select:none

### 4、屏蔽阴影 取消默认设置：
    -webkit-appearance:none

### 5、css3多文本换行
    overflow:hidden;
    text-overflow:ellipsis;
    display:-webkit-box;
    -webkit-line-clamp:2;
    -webkit-box-orient:vertical;

### 6、Retina屏幕高清图片
    selector {
          background-image: url(no-image-set.png);
          background: image-set(url(foo-lowres.png) 1x,url(foo-highres.png) 2x) center;
    }

### 7、移动端点透事件
    1 尽量都使用touch事件来替换click事件。
    2 阻止a链接的click的preventDefault

### 8、快速回弹滚动
    overflow:auto;
    -webkit-overflow-scrolling:touch; 

### 9、设置placeholder时候 focus时候文字没有隐藏
    input:focus::-webkit-input-placeholder{
      opacity:0;
    }

### 10、添加到主屏后的标题
    <metaname="apple-mobile-web-app-title"content="标题">

### 11、忽略数字自动识别为电话号码
    <metacontent="telephone=no"name="format-detection" /> 

### 12、忽略识别邮箱
    <metacontent="email=no"name="format-detection" />

### 13、定义浏览器点击行为
    <a href="tel:020-10086">打电话给:020-10086</a>
    <a href="sms:10086">发短信给: 10086</a>
    <a href="mailto:me@22278.club">发送邮件: me@22278.club</a>

### 14、定义上传文件类型和格式
    <input type=file accept="image/*">
    上面的文件上传框中，accept 可以限制上传文件的类型，参数为 image/* 是所有图片类型，点击会弹出图库，也可以指定图片格式，
    参数设置成 image/png 则可以限制图片类型为png；
    参数如果为 video/* 则是选择视频的意思；
    accept 还可以设置多个文件格式，语法为 accept="image/gif, image/jpeg" ；

### 15、使用box-shadow改变(挡住)表单自动填充后的黄色
    input:-webkit-autofill, textarea:-webkit-autofill, select:-webkit-autofill{
        box-shadow:inset 0 0 0 1000px #fff;
    }

### 16、点击去掉阴影背景
    -webkit-tap-highlight-color: rgba(0,0,0,0);

