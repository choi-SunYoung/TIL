오늘 오전에 듣는 국비수업에서 j-query를 이용한 슬라이드 배너 만드는 것을 배웠다.

CSS만으로, 그리고 JavaScript로도 만들 수 있을 것 같아서 만들어본 슬라이드 배너.

```html
<!--HTML-->
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>1124</title>
  <link href="style.css" rel = "stylesheet" />
</head>


<body>
  <div id = "wrap">
    <header></header>
    <div id = "banner">
      <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <!--<li>
          <a href = "#">
            <img src = "img/img1.jpg" />
          </a>
        </li>
        <li>
          <a href = "#">
            <img src = "img/img2.jpg" />
          </a>
        </li>
        <li>
          <a href = "#">
            <img src = "img/img3.jpg" />
          </a>
        </li>
        <li>
          <a href = "#">
            <img src = "img/img4.jpg" />
          </a>
        </li>-->
      </ul>
    </div>
  </div>
</body>
</html>
```

background에 색을 줘서 슬라이드 하고 이미지를 삽입해서도 해보았다.





```css
/*css: animation 활용*/
*{
  margin: 0;
  padding: 0;
}
ul, ol, li{
  list-style: none;
}
img{
  border: none;
}
#wrap{
  margin: 0 auto;
  width: 1200px;
}
a{
  text-decoration: none;
  color: inherit;
}
/* reset............and wrap...................................... */
header{
  width: 1200px;
  height: 120px;
  background: #ccc;
}
#banner li:nth-child(1){
  background:grey;
}
#banner li:nth-child(2){
  background:gold;
}
#banner li:nth-child(3){
  background:green;
}
#banner li:nth-child(4){
  background:purple;
}
#banner{
  width: 1200px;
  height: 800px;
  overflow: hidden;				/*banner박스를 벗어나는 것은 숨긴다.*/
}
#banner ul li{
  width: 1200px;
  height: 800px;
  float: left;		    		/*li들을 왼쪽으로 붙힌다.*/
}
#banner ul{
  width: 4800px;				/*ul 넓이를 li넓이*li갯수로 설정한다. */
  height: 800px;
  animation:slide 8s infinite;  /*8초마다 무한으로 슬라이드한다.*/
}
@keyframes slide {
      0% {margin-left:0;}       /*0 ~ 10  : stop*/
      10% {margin-left:0;}      /*10 ~ 25 : slide*/
      25% {margin-left:-100%;}  /*25 ~ 35 : stop*/
      35% {margin-left:-100%;}  /*35 ~ 50 : slide*/
      50% {margin-left:-200%;}  /*50 ~ 60 : stop*/
      60% {margin-left:-200%;}  /*60 ~ 75 : slide*/
      75% {margin-left:-300%;}  /*75 ~ 85 : stop*/
      85% {margin-left:-300%;}  /*85 ~ 100 : slide*/
      100% {margin-left:0;}     /*처음으로*/
    }
```



결과물: 



<img src="C:\Users\chois\Desktop\bg.gif" style="zoom:50%;" /><img src="C:\Users\chois\Desktop\img.gif" style="zoom:50%;" />