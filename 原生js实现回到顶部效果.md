* 1.简单粗暴型

  ```js
    window.scrollTo(0, 0); // 第一个参数为x轴偏移值，第二个为y轴偏移值
  ```

* 2.带有动画效果

 ```js
    const goTop = setInterval(() => {
      let Yoffset = window.pageYOffset
      console.log(Yoffset)
      if (Yoffset) {
        window.scrollTo(0, Yoffset - 20)
      } else {
        clearInterval(goTop)
      }
    }, 16);
  ```

  ```js
    function gotop() { 
      let scroolHeight = document.documentElement.scrollTop || document.body.scrollTop;
      if(scroolHeight > 0) { 
        window.requestAnimationFrame(gotop); 
        window.scrollTo(0, scroolHeight - scroolHeight / 50) 
      }
    };
    gotop()
  ```
