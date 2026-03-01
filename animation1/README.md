## 相册类动画

### 旋转相册-Y轴旋转
- index：https://codepen.io/hoanghien0410/pen/MMPaqm
- index2：原理版👆
- index3：自行实现版

```
npx parcel index.html
npx parcel index2.html
npx parcel index3.html


旋转相册-水平，思路：
1. 3D效果的核心：html + perspective: 1000px + body/#scene/img 均transform-style: preserve-3d
2. 静态：相框relative + 图片absolute，给每张图片分配rotateY + translateZ(指定半径)
3. 无干预动态旋转：旋转图片的容器而非图片，改变容器的旋转rotateY
4. 有干预旋转：监听鼠标的拖动，根据clientX的偏移计算delta值乘以系数作为图片容器的旋转角度
5. 图片纵向倒影效果：-webkit-box-reflect: below 10px linear-gradient(transparent, transparent, #0005);
```



## TODO
- [ ] X轴旋转
- [ ] 老虎机
- [ ] 转盘
- [ ] coverflow
- [ ] swiper