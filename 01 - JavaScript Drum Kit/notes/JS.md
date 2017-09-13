## JavaScript 部分

**基本思路**
* 检测键盘按下的动作 -- 监听 ```keydown``` 事件
* 键盘被按下时，播放音效 --``` audio.play()```
* 按键被按下、播放音效的同时，播放动画 -- ```Element.classList.add('className')```
* 在动画结束后，移除动画，不然在第一次点击之后，再次点击就不会有任何效果 ```Element.classList.remove('className')```

**keydown() 事件**

* 功能：检查用户是否按了键盘上指定的键
* 语法：```keydown(keycode)```
* 参数 ```keycode``` ：```keyCode``` 枚举类型 或``` integer``` 类型，指明要检测的按键或某个键的 ```ASCII``` 值 返回``` Boolean```。如果用户按了``` keycode ```参数指定的按键，返回 ```true``` ，否则返回``` false``` ，如果参数``` keycode``` 值为``` null ```，则 ```keydown()``` 函数返回 ```null``` 。
* 注意：完整的``` key press ```过程分为两个部分：1.按键被按下；2.按键被松开
* 当按键被按下的时候，发生``` keydown ```事件
* 不同浏览器对``` keydown keyup ```事件的界定不同（下面记录为 中文输入法下 ）
    * ```firfox```：输入触发```keydown```，回车确认输入触发```keyup```
    * ```chrome```：输入触发```keydown```、keyup，回车确认输入只触发```keydown```
    * ```IE```：输入触发```keydown```、```keyup```，回车确认输入触发```keydown```，```keyup```
    * ```Safari```：输入触发```keydown```、```keyup```，回车确认输入触发```keydown```，```keyup```
    * ```opera```：输入触发```keydown```、```keyup```，回车确认输入触发```keydown```，```keyup```
* js 里面常用的键盘事件对应的键码
```
keyCode 8 = BackSpace BackSpace
keyCode 9 = Tab Tab
keyCode 12 = Clear
keyCode 13 = Enter
keyCode 32 = space  
keyCode 35 = End
keyCode 36 = Home
keyCode 37 = Left
keyCode 38 = Up
keyCode 39 = Right
keyCode 40 = Down
keyCode 46 = Delete

yCode 65 = a A
keyCode 66 = b B
keyCode 67 = c C
keyCode 68 = d D
keyCode 69 = e E EuroSign
keyCode 70 = f F
keyCode 71 = g G
keyCode 72 = h H
keyCode 73 = i I
keyCode 74 = j J
keyCode 75 = k K
keyCode 76 = l L
keyCode 77 = m M mu
keyCode 78 = n N
keyCode 79 = o O
keyCode 80 = p P
keyCode 81 = q Q at
keyCode 82 = r R
keyCode 83 = s S
keyCode 84 = t T
keyCode 85 = u U
keyCode 86 = v V
keyCode 87 = w W
keyCode 88 = x X
keyCode 89 = y Y
keyCode 90 = z Z
keyCode 112 = F1
keyCode 113 = F2
keyCode 114 = F3
keyCode 115 = F4
keyCode 116 = F5
keyCode 117 = F6
keyCode 118 = F7
keyCode 119 = F8
keyCode 120 = F9
keyCode 121 = F10
keyCode 122 = F11
keyCode 123 = F12

```
> 其中``` a ~ z A ~ Z ```的``` keycode ```与相对应的``` ASCII``` 是一致的

**audio.play() 事件**
* ```play()``` 方法： 开始播放当前的音频或者视频
* 语法：```audio | video.play()   (audioObject.play() )```
* 参数:```None```
* 返回值:没有返回值
* ```eg```
``` 
var x = document.getElementById("myAudio");
function playAudio(){
    x.play();
}
function pauseAudio(){
    x.pause();
}

```


**Object.classList.add('className') / Object.classList.remove('className')**

* 用途:此方法为 用 ```JavaScript ```为 元素添加``` class  ```
* ```eg ```
*高级浏览器*
    *``` document.getElementById('body').classList.add('addedcClass');  ```
    * ``` document.getElementById('body').classList.remove('removedcClass');  ```
*不支持``` classList ```的浏览器*
    * ```document.getElementById('body').className += 'addedcClass';  ```

**classList 属性**
* 语法
    * element.classList
* 定义和用法
    * classList 属性返回元素的类名,作为 DOMTokenList 对象
    * 该属性用于在元素中 添加 / 移除 / 切换 css 类
    * classList 属性是只读的,但是可以使用 add() remove()方法修改
* 方法
    * add(class,class2,...)
        * 在元素中添加一个或多个类名.如果指定的类名已经存在,则不会添加.
    * contains(class)
        * 返回布尔值,判断指定的类名是否存在,存在 true ,不存在 false
    * item(index)
        * 返回类名在元素中的索引值(index 从 0  开始),如果索引值在区间范围外则返回 null
    * remove(class1,class2, ...)
        * 移除元素中一个或多个类名,并且,移除**不存在**的类名,不会报错
    * toggle(class,*true|false*)
        * 在元素中切换类名
        * 第一个参数为要在元素中移除的类名,并返回false,如果该类名不存在则会在元素中添加类名,并返回 true
        * 第二个参数为**可选参数**,这个 布尔值 用于设置元素是否强制添加或者移除类,不管该类名是否存在
    **注意**
    * IE 或 Opera12 及更早版本 不支持第二个参数


**data-key**
* 这是一个自定义属性,如果没有合适的属性可以定义一个参数,则就可以通过 data-* 的方式自定义页面的数据.在这里作用为:通过 data-key 将页面展示的内容与 audio 关联起来.

**display:flex**
* 涉及到 flex 布局   [参考资料](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)

**flex:1**
* flex 属性是 flex-grow  flex-shrink  flex-basis  的缩写.默认值为 0,1,auto.后两个属性是可选的

```
.item{
    flex: none | [ <'flex-grow'> <'flex-shrink'> ? || <'flex-basis'> ]
}
```
> [  ] 表示参数可选
* [参考资料](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)(4.5 flex属性)
    
**document.querySelector()**
* 返回文档中匹配指定的选择器组的第一个元素
* 如果没有找到匹配的元素,则返回 null ,如果找到多个,则返回第一个匹配到的元素
* [参考文章](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/querySelector)
* 语法
    * element = document.querySelector(selectors)
    * element 是一个 element 对象 ( DOM )
    * selectors 是一个字符串,包含一个或者多个 CSS 选择器,多个则以逗号隔开
    * 比如: var el = document.querySelector(".myclass");
        * 会返回当前文档中第一个类名为 "myclass" 的元素
* 与本项目中 audio = document.querySelector(`audio[data-key="${e.keyCode}"]`); 类似的一个例子为:
```
<div class="user-panel main">
    <input name="login"/> //这个标签将被返回
</div>

<script>
    var el = document.querySelector("div.user-panel.main input[name=login]");
</script>
```

**audio.currentTime = 0**
* 