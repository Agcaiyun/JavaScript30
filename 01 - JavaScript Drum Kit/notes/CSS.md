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

