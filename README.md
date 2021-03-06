# LazyLoad
改进版的 LazyLoad 懒加载库；

### LazyLoad 用法：
> 此 LazyLoad 为改进版，支持 jQuery 和 Zepto.js，比官方提供的版本有更强大的功能：增加了背景图和 class 的动态加载功能；
```html
<img class="lazy" data-src="http://www.abc.com/abc.png" alt="动态加载图片">
<div class="lazy" data-class="XXX">动态加载 XXX 类</div>
<div class="lazy" data-src="http://www.abc.com/abc.png">动态加载背景图</div>
```
```js
$('.lazy').lazyload({
  threshold : 450, // 离可见区域的距离 
  effect : false, // 可选，默认为 'show'；为 false 时，没有任何视觉效果；
  skip_invisible: true // 可选，是否跳过不可见内容
});
```

自定义事件，在图片显示时响应
```js
$('.lazy').on('appear', function(e){
    console.log(e.target);
});
```
自定义事件，在图片显示完成后响应
```js
$('.lazy').on('appeared', function(e){
    console.log(e.target);
});
```

[LazyLoad 更多用法介绍](http://www.appelsiini.net/projects/lazyload)
