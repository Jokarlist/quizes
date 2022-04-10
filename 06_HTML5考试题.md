1. ```markdown
   - 标签语义化指的是标签名是有具体语义含义的
   - 使用其的好处是在布局时描述结构上会更加清晰
   ```

   参考答案：

   ```markdown
   - HTMl标签语义化，简单来说，就是让标签有含义，给某块内容用上一个最恰当最合适的标签，使页面有良好的结构，页面元素有含义，不论是谁都能够看懂这块内容是什么，并且有利于搜索引擎
   
   - 标签语义化的好处：
     1. HTML结构清晰
     2. 代码可读性较好
     3. 无障碍阅读
     4. 搜索引擎可以根据标签的语义确定上下文和权重问题
     5. 移动设备能够更完美的展现网页（对css支持较弱的设备）
     6. 便于团队维护和开发
   ```

   

2. ```markdown
   - DOCTYPE是区分渲染文档的标准模式和混杂模式所用
   - 文档开头标上`<!DOCTYPE html>`则表示标准模式，不标则表示混杂模式
   - 标准模式是基于html5的语法，混杂模式是除了h5的语法还会去兼容之前的语法
   ```

   参考答案：

   ```markdown
   - DOCTYPE的作用：<!DOCTYPE>声明叫做文件类型定义（DTD），声明的作用是为了告诉浏览器该文件的类型。让浏览器解析器知道应该用哪个规范来解析文档。<!DOCTYPE>声明必须在 HTML 文档的第一行，这并不是一个 HTML 标签。
   
   - 标准模式和混杂模式：
     - 标准模式（Standards mode）：浏览器按照 W3C 标准解析代码
     - 混杂模式（Quirks mode）：浏览器用自己的方式解析代码
   
   - 区分标准模式和混杂模式：
     - 如果文档包含严格的 DOCTYPE ，那么它一般以标准模式呈现
     - 有 URI 的过渡 DTD ——标准模式；没有 URI 的过渡 DTD ——混杂模式
     - DTD不存在或者格式不正确——混杂模式
     - HTML5 没有严格和混杂之分。HTML5 没有 DTD ，因此也就没有严格模式与混杂模式的区别，HTML5 有相对宽松的语法，实现时，已经尽可能大的实现了向后兼容。
   
   - 意义：严格模式与混杂模式存在的意义与其来源密切相关，如果说只存在严格模式，那么许多旧网站必然受到影响，如果只存在混杂模式，那么会回到当时浏览器大战时的混乱，每个浏览器都有自己的解析模式。
   ```

   

3. ```markdown
   - alt属性是当元素想要展示的内容因某些原因而未能展示时所用来替代展示的标识，title属性表示的是元素附加的提示信息
   ```

   参考答案：

   ```markdown
   - alt作为图片的替代文字出现，title作为图片的解释文字出现
   - alt属性应用较少，如img、area、input中；title应用较多，如a、form、input、还有div、p这些块级元素都可以用
   - alt仅作为标签属性，title也可以是标签，它是网页的标题标签
   ```

   

4.  `AB`

5.  `AD`

6. ```markdown
   - Canvas是一个可以使用脚本例如js来绘制图形的html元素
   ```

   参考答案:

   ```markdown
   - Canvas是h5新增的一个标签
   - HTML5 的 canvas 元素使用 JavaScript 在网页上绘制图像。
   - 画布是一个矩形区域，您可以控制其每一像素。
   - canvas 拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。
   ```

   

7. ```markdown
   - SVG是xml的分支语言之一，用于标记可缩放的矢量图形；
   - 其他图像格式放大之后图像会失真，SVG图像则不会失真，且通常动画较少或较简单，适合大面积贴图
   ```

   答案：

   ```markdown
   - 定义：
   - SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
   - SVG 用于定义用于网络的基于矢量的图形
   - SVG 使用 XML 格式定义图形
   - SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
   - SVG 是万维网联盟的标准
   
   - 优势：
   - SVG 图像可通过文本编辑器来创建和修改
   - SVG 图像可被搜索、索引、脚本化或压缩
   - SVG 是可伸缩的
   - SVG 图像可在任何的分辨率下被高质量地打印
   - SVG 可在图像质量不下降的情况下被放大
   ```

   

8. ```markdown
   - Canvas渲染的是位图，SVG渲染的是矢量图
   - Canvas多用脚本js来操作，SVG多用css和html来操作
   ```

   参考答案：

   ```markdown
   - canvas：
     - 依赖分辨率
     - 不支持事件处理器
     - 弱的文本渲染能力
     - 能够以 .png 或 .jpg 格式保存结果图像
     - 最适合图像密集型的游戏，其中的许多对象会被频繁重绘
   
   - svg：
     - 不依赖分辨率
     - 支持事件处理器
     - 最适合带有大型渲染区域的应用程序（比如谷歌地图）
     - 复杂度高会减慢渲染速度（任何过度使用DOM的应用都不快）
     - 不适合游戏应用
   ```

   

9. `B`

   答案：C

10. `C`

    

11. `canvas元素所参照的变换坐标系`

    答案：`画布坐标系`

    

12. `BC`

    解析：HTML5 `<canvas>` 标签用于绘制图像，需要js脚本来驱动，通过jquery选择器选中的元素返回为jq对象，不能直接调用canvas中的执行期上下文，需要选中对象中索引值为零的dom元素，再去调用执行期上下文。

13.  `ABCD`

14. `ABD`

    解析：可以使用poster属性指定占位图像，可以使用width height属性设置视频尺寸，如果使用了muted属性，视频从一开始就处于静音状态

15. `B`

    解析：contenteditable 属性规定元素内容是否可编辑。如果元素未设置 contenteditable 属性，那么元素会从其父元素继承该属性。

16. `D`

    

17. `draggable`、`dragstart`、`dragover和drop`

    答案：`draggable`、`dragstart`、`dragend`

    

18.  ```html
     <!DOCTYPE html>
     <html>
         <head></head>
         <body></body>
     </html>
     
     <!-- 答案 -->
     <!DOCTYPE html>
     <html>
         <head>
         	<meta charset="UTF-8">
             <title>Document</title>
         </head>
         <body>
         	webContent
         </body>
     </html>
     ```
     
     
     
19.  `ABCD`

20. `C`

    答案：D

    解析：sessionstorage不在不同的浏览器共享，即使同一页面

    

21. `ctx.createLinearGradinent()`、`gradient.addColorStop()`

    

22. `resize`、`blur`

    

23. `BCD`

    答案：BC
