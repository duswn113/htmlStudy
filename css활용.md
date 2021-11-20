


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
[결과보기](https://codepen.io/Leeyeonju/pen/porYQvp){: target="_blank"}

<br>