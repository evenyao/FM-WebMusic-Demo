# Music
大屏页面音乐播放器

WebMusic项目

## 预览地址

## 版本相关
### 2018.8.28
v0.1：完成静态页面效果与布局

## 布局要点
### 响应式
由于该作品可能会放置到宽度很长的设备上进行播放，类似于移动端相当于 `宽度vw` 进行布局自适应。
但该项目中，我们应该针对 `高度vh` 进行布局自适应，因为在实际情况中，用户的设备可能宽度很宽，如果使用 `vw` 会导致布局整体效果不佳。

### 毛玻璃 Background 效果
```CSS
.bg {
  position: absolute;
  z-index: -1;
  left: -10px;
  top: -10px;
  bottom: -10px;
  right: -10px;
  background: url("2.jpg") no-repeat center;
  background-size: cover;
  filter: blur(4px);
}
.bg::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  right: 0;
  background: rgba(0,0,0,0.4);
}
```
### flex 布局
巧用 flex 使 iconfont 等比布局
```CSS
main .aside .actions {
  display: flex;
  margin-top: 4vh;
}
main .aside li {
  flex:1;
  text-align: center;
}
```


### footer 绝对定位
```CSS
footer .icon-left {
  position: absolute;
  left: -10vh;
}
footer .icon-right {
  position: absolute;
  right: -10vh;
}
```
