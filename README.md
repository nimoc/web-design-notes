# 前端写给设计的设计注意事项

> Web 设计和 Web 前端都应该仔细阅读此文档，会减少因为设计不合格导致的返工。

Web 设计和广告设计有很大区别。在视觉上广告设计只要颜色符合规范都可以100%打印出来。

Web 设计因为要在浏览器中实现，有时还需要『动』起来，在设计时有一定的限制。

## 尺寸

### 最小宽度
![width-980](./media/width-980.png)

Github 页面最小宽度是 980px，当窗口大小小于 980px 时候会出现滚动条。

![width-980-scroll.png](./media/width-980-scroll.png)

网页最小宽度是根据浏览者的电脑分辨率来定。

例如浏览者的分辨率是 1280x800
则最小宽度不可大于 *1240* `1280 - 80 = 1240`，因为网页可能会出现滚动条或一些工具栏。所以需要减去 80 像素。

> 下图中浏览器左侧有工具栏，右侧存在滚动条

![](./media/maxthon.png)

### 响应式设计

响应式设计规范可参考 [https://github.com/ColdXu/grid-design](https://github.com/ColdXu/grid-design)

### 移动设备 Retina

手持设备的设计稿基准尺寸为 375px，普通屏显示正常，但在 Retina 屏幕下会出现图片模糊问题。 

对于 Retina 屏幕，为了达到高清效果，视觉稿的画布大小会是基准的2倍，最终设计稿尺寸是750px 

> iphone6 DPI 是 375 所以此处 设计稿基准尺寸是 375px,如果要兼容 iphone4/4s/5 则基准是 320（设计稿尺寸是 640px）


## 文字溢出

某些文字由程序输出的文字长度是无法确认的，需要设计时考虑文字超出容器大小时候的溢出处理方式。

### ...

> 当文字超过一定字数后会出现 `...`
![text-overflow](./media/text-overflow.png)

### 裁剪

> 一行文字占 20px ，最多只显示2行，超过2行的文字不显示
![text-overflow-hidden](./media/text-overflow-hidden.png)
![text-overflow-hidden-2](./media/text-overflow-hidden-2.png)

### 提示
> 当鼠标划入时出现完整内容信息
![text-overflow-tip](./media/text-overflow-tip.png)