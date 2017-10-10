## 기본 이벤트와 이벤트 전달

이벤트 객체의 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| preventDefault() | 기본 이벤트를 제거 |
| stopPropagation() | 이벤트 전달을 제거 |

예제

```javascript
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script src='http://code.jquery.com/jquery-latest.min.js'></script>
    <style>
        *{
            margin: 5px;
            padding: 5px;
            border: 3px solid black;
        }
    </style>
</head>
<body>
    <h1>
        <a href="https://github.com/tjdtjq91">github</a>
    </h1>

    <script>
        $(document).ready(function () {
            $("a").click(function (event) {
                $(this).css("background-color", "blue");
                event.preventDefault();
            });

            $("h1").click(function () {
                $(this).css("background-color", "red");
            })
        });
    </script>
</body>
```
