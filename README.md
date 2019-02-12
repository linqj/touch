1、什么是移动端的 Touch事件？在移动端 Touch事件可以细分成三种，分别是： touchstart、 touchmove和 touchend，并且 touch事件必须要用 addEventListener去监听。

touchStart当手指触碰到屏幕的时候触发

touchmove当手指在屏幕上不断移动的时候触发

touchend当手指离开屏幕的时候触发
// 手指触碰到屏幕时触发

element.addEventListener('touchstart',function(e){  
// 打印的事件对象
console.log(e);})

2、如果只要一次查找就可得到元素时，首选getXXXByXXX ；

如果需要经过多级查找，才能得到元素时，首选querySelector；
3、其实这三种返回的对象，都是表示用户触摸事件时的手指信息，之所以是一个伪数组，是因为有可能出现多指同时触摸，但是在实际工作中一般不去考虑多指的情况。而它们唯一的区别就是在 touchstart和 touchmove事件的时候， changedTouches、 targetTouches、 touches都能获取到手指的信息，但是在 touchend事件的时候， targetTouches、 touches对象是不能返回离开屏幕时的手指信息，只有 changedTouches对象能返回。