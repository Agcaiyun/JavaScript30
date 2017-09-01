## CSS 部分

**background-size**
* 语法：``` background-size: length | percentage | cover | contain;```
* ```length``` 
    * 设置背景图像的高度和宽度，第一个值设置宽度，第二个值设置高度，如果只设置一个值，则第二个值会被设置为 ```auto```
* ```percentage``` 
    * 以**父元素**的百分比来设置背景图像的宽度和高度，两个值分别是 宽 高 ，如果只设置一个，则第二个值被设置为 ```auto```
* ```cover```
    * 把背景图像扩展到足够大，以使背景图像完全覆盖背景区域，图像背景的某些部分也许无法显示在背景定位区域中。
* ```contain```
    * 把图像扩展到最大尺寸，以使其宽度和高度完全适应内容区域

**display:flex;**
* [参考资料](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
* 布局的传统解决方案,基于 盒模型,依赖 dispaly 属性 +  position 属性 + float 属性.它对于那些特殊布局非常不方便,比如:垂直居中 就不容易实现
* 2009年,W3C 提出了一种新的方案 --- Flex 布局. 它可以简便 完整 响应式 地实现各种页面布局.目前,它已经得到了所有浏览器的支持,这意味着,现在就能很安全的使用这项功能.
* 设置为 flex 布局后,子元素的 float clear vertical-align 属性将失效.

**min-height:100vh**
* vh :```CSS3```中 相对长度单位,表示相对视口高度(```Viewport Height```),```1vh``` = 1% * 视口高度.
* ```CSS3 ```中单位 ```px``` , ```em``` , ```rem``` ,``` vh``` , ```vw``` , ```vmin``` , ```vmax ```的区别
    * ``` px ```: 绝对单位,页面按确定的像素进行展示
    * ``` em ```: 相对单位,相对与 父级 字体的大小,所以整个页面来讲```, 1em ```并不一定是一个固定的值.
    * ``` rem``` : 相对单位,比``` em ``` 多了一个``` r``` ,这个 ```r ```可以理解为 ```root ```,即相对于**根节点**的字体大小来计算,这是``` CSS3``` 新增属性.
    * ``` vw``` : ```viewpoint width``` ,视窗宽度,``` 1vw``` = 1% * 视窗宽度
    * ``` vh``` : ```viewpoint height ```, 视窗高度,```1vh``` = 1% * 视窗高度
    * ``` vmin ```:``` vw ```和``` vh``` 中 比较小的那一个数值
    * ``` vmax ```: 与``` vmin ```类似,表示 ```vw ```和``` vh ```中比较大的那一个数值
* 提示:
    * ```rem``` 中 :```chrome``` 限制字体最小为``` 12px ```,就算设置为``` 10px```,那么最后也会以``` 12px``` 来显示,并且子节点``` rem ```计算的参照也还是 ```12px ```.

**border: .4rem solid black;**
* 其中  ``` .4rem``` 中  ```.4  ``` 表示的是 ``` 0.4 ```
> 啊,自己好傻,一时间都没反应过来,竟还傻傻的  ```Googl``` 了

**transition:all .07s ease;**
* ```CSS3 transition ``` 属性
* ```transition  ```是一个复合属性,其中可以设置四个过渡属性
* 语法:
    * ```transition:property ```     ```duration  ``` ``` timing-function   ```     ```delay ```;
        *``` transition-property``` : 规定设置过渡效果的``` CSS ```属性的名称
            * ```transition-property : none | all | property```
            > 其中,```property ```定义应用过渡效果的 ```CSS ```属性名称列表,列表以逗号分隔
        * ```transition-duration ```: 规定完成过渡效果需要的时间(秒 或者 毫秒)
            * 默认值为``` 0 ```,即 没有任何效果
            * ```JS ```语法 :``` object.style.transitionDuration = "5s"```
        *``` transition-timing-function``` : 规定速度效果的速度曲线
            * [相关知识简介](http://www.w3school.com.cn/cssref/pr_transition-timing-function.asp)
            * [相关效果演示](http://www.w3school.com.cn/tiy/t.asp?f=css3_transition-timing-function2)
        *``` transition-delay``` : 定义过渡效果何时开始(即在过渡效果开始之前需要等待的时间)
            * 默认值 为``` 0```

**background: rgba(0,0,0,0.4)**
* 最后一位表示透明度
* 相比 直接这是``` opacity ```的优点
    * 在设置透明度的时候,如果设置为 ```opacity , ```那么 子元素 比如里面的文字,也会变得有透明度
    * 如果设置为``` background-color:rgba() ```这种形式,里面的子元素 比如文字,就不会变的有透明度
    * 往往 ```background-color:rgba() ```会更符合我们的需求

**text-shadow**
* text-shadow : h-shadow  v-shadow  blur  color;
* [效果演示](http://www.w3school.com.cn/tiy/c.asp?f=css_text-shadow)
* 省略的长度是 0 

**transform**
* transform 属性向元素应用 2D 或 3D 转换.我们可以对元素进行旋转/缩放/移动 或 倾斜
* transform:scale(x,y) 
    * 定义 2D 缩放
    * 如果参数中只有一个数值,则认为 x y 设置为 相同的数值
* [参考资料](http://www.w3school.com.cn/cssref/pr_transform.asp)

