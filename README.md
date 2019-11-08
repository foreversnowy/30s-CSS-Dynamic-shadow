  
**30秒的CSS - 动态阴影**

<br>

**未加阴影时**
```html
    <div class="shadow"></div>
```
```css
    .shadow {
        width: 200px;
        height: 200px;
        background: linear-gradient(75deg, #18dcff, #c56cf0);
    }
```
![未加阴影前](https://forever-1258828479.cos.ap-beijing.myqcloud.com/myblog/page/shadow/1.png)

***
<br>

**添加阴影后**
```css
    .shadow {
        position: relative;
        width: 200px;
        height: 200px;
        background: linear-gradient(75deg, #18dcff, #c56cf0);
    }

    .shadow::after {
        position: absolute;
        content: '';
        width: 100%;
        height: 100%;
        top: 4px;
        left: 3px;
        /* 背景颜色继承 */
        background: inherit;
        /* 模糊 */
        filter: blur(0.4rem);
        /* 透明度 */
        opacity: 0.7;
    }
```
![未加阴影前](https://forever-1258828479.cos.ap-beijing.myqcloud.com/myblog/page/shadow/2.png)  

是不是感觉生动了许多呢?  

> [项目地址](https://github.com/foreversnowy/30s-CSS-Dynamic-shadow)

***
<br>

**相关资料**

>[CSS3 linear-gradient](https://www.runoob.com/cssref/func-linear-gradient.html)  
>[CSS3 filter](https://www.runoob.com/cssref/css3-pr-filter.html)  
>[CSS3 opacity](https://www.w3school.com.cn/cssref/pr_opacity.asp)
