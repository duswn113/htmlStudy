# Input 태그

<br>

## 여러개의 라디오태그 하나만 선택 되게
- 모든 라디오태그의 name 값을 동일하게 한다.
```html
<form action="target.html" method="get">
    <div class="test1">
        <div>
            <input type="radio" name="problem" id="radio1" checked>
            <label for="radio1">틀리는문제는 문제는무넺는</label>
        </div>
        <div>
            <input type="radio" name="problem" id="radio2">
            <label for="radio2">틀리는문제는 문제는....</label>
        </div>
    </div>
    <button>저장</button>
</form>
```
```css
input[type="radio"]:checked + label {
    font-weight: bold;
}
```

<br>