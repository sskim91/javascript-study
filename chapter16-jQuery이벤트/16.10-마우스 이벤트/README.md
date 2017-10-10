## 마우스 이벤트

| 이벤트 이름 | 설명 |
| :------------- | :------------- |
| click | 마우스를 클릭할 때 발생 |
| dblclick | 마우스를 더블 클릭할 때 발생 |
| mousedown | 마우스 버튼을 누를 때 발생 |
| mouseup | 마우스 버튼을 뗄 때 발생 |
| mouseenter | 마우스가 요소의 경계 외부에서 내부로 이동할 때 발생 |
| mouseleave | 마우스가 요소의 경계 내부에서 외부로 이동할 때 발생 |
| mousemove | 마우스가 움직일 때 발생 |
| mouseout | 마우스가 요소를 벗어날 때 발생
| mouseover | 마우스를 요소 안에 들어올때 발생  |

예제

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <style>
        .outer {
            width: 200px;
            height: 200px;
            background: orange;
            padding: 50px;
            margin: 10px;
        }

        .inner {
            width: 100%;
            height: 100%;
            background: red;
        }
    </style>
</head>
<body>

<div class="outer">
    <div class="inner"></div>
</div>

<script>
    $(document).ready(function(){
        $(".outer").mouseover(function () {
            $("body").append("<h1>mouseover</h1>");
        }).mouseenter(function () {
            $("body").append("<h1>mouseenter</h1>");
        })
    });
</script>
</body>
</html>
```

mouseover 이벤트는 이벤트 버블링을 적용  
반면 mouseenter 이벤트는 문서 객체의 안에 있는지 외부에 있는지 판단
