# Web前端写给Web设计师的注意事项

> Web 设计和 Web 前端都应该仔细阅读此文档，会减少因为设计不合理导致的返工。

Web 设计和广告设计有很大区别。在视觉上广告设计只要颜色符合规范都可以100%打印出来。

Web 设计因为要在浏览器中实现，有时还需要『动』起来，在设计时有一定的限制。

**前端同行应该以此文档作为审核设计稿的依据，不应该拿到设计稿直接开发。**

有任何问题请 [参与讨论](https://github.com/nimojs/web-desgin-notes/issues/new) [讨论列表](https://github.com/nimojs/web-desgin-notes/issues)

> 点击右上角的 **[Watch](https://github.com/nimojs/web-desgin-notes/subscription)** 订阅本文档更新，点击 Star 收藏本书

---

<a name="hash_top" href="#hash_top"></a>

**索引**

1. [页面尺寸](#hash_size)
	1. [最小宽度](#hash_size_min-width)
	2. [响应式设计](#hash_responsive)
	3. [移动设备 Retina](#hash_retina)
2. [字体](#hash_font)
	1. [大小](#hash_font-size)
	2. [特殊字体](#hash_font-special)
	3. 字体图标
3. [内容溢出](#hash_text-overflow)
	1. [...](#hash_text-overflow-ddd)
	2. [裁剪](#hash_text-overflow-clip)
	3. [提示](#hash_text-overflow-tip)
4. PSD
	1. 图层命名
	2. Retina
	3. 标注
	4. 字体
5. 分页
6. 状态
	1. loading 加载中
	2. Hover 滑过
	3. error 加载出错
	4. empty 元素为空（常见于列表）
	5. 页面其他逻辑的状态（比如某些字段可选时候）
7. UI组件化
8. typo 内容排版样式
	1. 富文本编辑
	2. markdown
9. 技术团队审核设计稿

---

<a name="hash_size" href="#hash_top">Top</a>

## 页面尺寸

网页尺寸需要考虑浏览者的屏幕分辨率

<a name="hash_size_min-width" href="#hash_top">Top</a>

### 最小宽度
![width-980](./media/width-980.png)

Github 页面最小宽度是 980px，当窗口大小小于 980px 时候会出现滚动条。

![width-980-scroll.png](./media/width-980-scroll.png)

网页最小宽度是根据浏览者的电脑分辨率来定。

例如浏览者的分辨率是 1280x800
则最小宽度不可小于 *1240* `1280 - 80 = 1200`，因为网页可能会出现滚动条或一些工具栏。所以需要减去 80 像素。

> 下图中浏览器左侧有工具栏，右侧存在滚动条

![](./media/maxthon.png)

<a name="hash_responsive" href="#hash_top">Top</a>

### 响应式设计

响应式设计规范可参考 [https://github.com/ColdXu/grid-design](https://github.com/ColdXu/grid-design)

<a name="hash_retina" href="#hash_top">Top</a>

### 移动设备 Retina

手持设备的设计稿基准尺寸为 375px，普通屏显示正常，但在 Retina 屏幕下会出现图片模糊问题。 

对于 Retina 屏幕，为了达到高清效果，视觉稿的画布大小会是基准的2倍，最终设计稿尺寸是750px 

> iphone6 DPI 是 375 所以此处 设计稿基准尺寸是 375px,如果要兼容 iphone4/4s/5 则基准是 320（设计稿尺寸是 640px）

<a name="hash_font" href="#hash_top">Top</a>

## 字体

在网页中使用字体需要注意一些地方

<a name="hash_font-size" href="#hash_top">Top</a>

### 大小
内容性质字体大小不得小于 12px ，因为某些浏览器默认文字大小只能是 12px。网页中显示小于 12px 的文字会变形。

<a name="hash_font-special" href="#hash_top">Top</a>

### 特殊字体

> 这里的特殊字体指的是普通用户电脑中不存在的字体 ![font](./media/font.png)

由于程序输出的文字不建议使用中文特殊字体，因为想要在用户电脑中使用中文特殊字体需要在浏览器中加载字体文件。而中文字体文件体积至少 1MB 以上

推荐一个中文特殊字体生成平台，可以在不使用图片的情况下使用固定的少量文字。[WebFont](http://iconfont.cn/webfont/#!/webfont/index) 

若使用英文特殊字体，请将字体文件同 PSD 一并交付给前端。

<a name="hash_text-overflow" href="#hash_top">Top</a>

## 内容溢出

某些文字由程序输出的文字长度是无法确认的，需要设计时考虑文字超出容器大小时候的溢出处理方式。

<a name="hash_text-overflow-ddd" href="#hash_top">Top</a>

### ...

> 当文字超过一定字数后会出现 `...`
![text-overflow](./media/text-overflow.png)

<a name="hash_text-overflow-clip" href="#hash_top">Top</a>

### 裁剪

> 一行文字占 20px ，最多只显示2行，超过2行的文字不显示
![text-overflow-hidden](./media/text-overflow-hidden.png)

> 一行文字占 20px ，最多只显示1行，超过1行的文字不显示
![text-overflow-hidden-2](./media/text-overflow-hidden-2.png)

<a name="hash_text-overflow-tip" href="#hash_top">Top</a>

### 提示
> 当鼠标划入时出现完整内容信息
![text-overflow-tip](./media/text-overflow-tip.png)

<a name="hash_psd" href="#hash_top">Top</a>

