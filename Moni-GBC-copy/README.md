# Moni-GBC
## 总结
我暂且归结为熟练度问题吧。

2.根据学长说的和自己的体会，flex布局主要是用于搞一些比较规范的，整齐的排版，这适用于主要的地方的样式。对于一些小装饰，我们多用定位，比如absolute（子绝父相），让它不占据文档流，然后小装饰就可以随便跑了，小装饰比较自由。

## 动画展示
3.展示一下有技术含量的一部分吧：
先展示几个动画：

- 动画一
初始态
鼠标悬浮，NEWS的红条向右穿梭冒出来
鼠标离开，NEWS的红条向右穿梭归0

这个样式呢，首先这个红色条，是item的::after样式
::after样式必有的东西：
注意transform-origin的顺序哦：普通状态下是right，因为我们这里对应需要让NEWS的红条向右穿梭归0，代表最终指向右侧原点，使得scale为0
鼠标悬浮时为left，代表从左侧开始，向右侧过渡scale为1
综上来看：scale变大的时候，远离原点，变小时靠近原点哦。
注意： 要把item::after设置成块级元素，这样才能完全控制它的长宽哦。
```css
.item::after {
  content: "";
  position: absolute; /* 注意要保证在子绝父相的时候用 */
  top: 100%;
  left: 0;
  width: 100%;
  height: 0.5vh;
  transition: transform 0.3s ease;
  transform: scaleX(0);
  transform-origin: right; 
  background-color: red;
  display: block; /* 关键设置 */
}
然后我们需要给它设置动画
.item:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}
```
- 动画二（盒子里的是张png图片哦）
中间那个ContainerX里面图片变色的设置
重点是 `mix-blend-mode` 这个属性的设置。
它用来定义元素与其背景或其他元素的混合模式  
主要的选择：
- normal: 默认的混合模式，前景元素完全覆盖背景元素，没有任何混合效果。  
- multiply: 该模式会将前景和背景的颜色进行乘法运算，通常会让颜色变暗，适合阴影效果。  
- screen: 与 multiply 相反，使用屏幕效果来让颜色变亮。它将前景和背景的颜色进行反转后再进行乘法，常用来创建亮光效果。
```css
.item {
  display: inline-block; /* 必须先把a设置成块级元素! */
  position: relative;
}
.item img {
  display: block;
  width: 100%;
}
.item::after {
  content: "";
  position: absolute; /* 注意要保证在子绝父相的时候用 */
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  opacity: 0;
  background-color: red;
  transition: opacity 0.3s ease;
  mix-blend-mode: screen; /* 这个属性是绝对的主角 */
}
.item:hover::after {
  opacity : 1
}
```
没了.....值得吹的css动画就这俩了，中间四个item的动画我没复刻出来。
