


## 말줄임표 여러줄일 경우 

```html
<div class="sns">
    <p>더미텍스트 : 4줄이상 줄바꿈이 올수있도록 텍스트 작성 </p>
</div>
```
```css
.sns p { 
    width: 50%; /* 줄바꿈이 일어나도록 임의로 설정 */
    line-height: 25px;
    height:95px;
    font-size: 14px;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
}
```
[결과보기](https://codepen.io/Leeyeonju/pen/porYQvp)

<br><br>

## 구분자 만들기 
```html
    <ul class="test">
        <li>메뉴1</li>
        <li>메뉴2</li>
        <li>메뉴3</li>
        <li>메뉴4</li>
        <li>메뉴5</li>
    </ul>
```
```css
.test li { float: left; list-style: none;}
.test li:first-child ~ li::before {
    display: inline-block;
    content: '';
    height: 13px;
    width: 1px;
    background-color: black;
    margin: 0 20px;
}
```

<br><br>

## 애니메이션
```html
<div class="container">
    <div class="test"></div>
</div>
```

```css
.container { width: 300px;}
.test {
    width: 100%;
    height: 50px;
    background: red;
    animation: box 2s 3s 2;
    /* animation-name: box; */
    /* animation-duration: 2s; */
    /* animation-delay: 3s; */
    /* animation-iteration-count: 2; */
    /* animation-direction: reverse; */
    
}
@keyframes box {
    0% { width: 0 }
    50% {background-color: blue;}
    100% {width: 100%; }
}
```

<br>

## 햄버거버튼
- 제이쿼리 로딩 필요함
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<div class="hamber">
    <span class="top"></span>
    <span class="middle"></span>
    <span class="bottom"></span>
</div>
```
```css
.hamber { 
    position: absolute; 
    top:20px; 
    right: 20px;
    width: 35px;
    height: 27px;
    cursor: pointer;
}
.hamber span{
    width:33px;
    height:5px;
    background:cadetblue;
    display: inline-block;
    position: absolute;
    transition: all 0.4s;
}
.hamber .top{
    top: 0;
}
.hamber .middle{
    top:11px;
}
.hamber .bottom{
    top:22px;
}

.hamber.active .top {
    top : 11px; 
    background-color: black;
    transform: rotate(45deg);
}
.hamber.active .middle{
    opacity: 0;
}

.hamber.active .bottom {
    top:11px;
    background-color: black;
    transform: rotate(-45deg);
}

```
```js
$(function(){

    $('.hamber').click(function(){
       $(this).toggleClass('active');
    });
})
```

[결과보기](https://codepen.io/Leeyeonju/pen/oNeKKQN)