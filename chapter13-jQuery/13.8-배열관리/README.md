## 13.8 배열 관리

jQuery로 배열을 관리할 때는 each() 메서드를 사용한다.  
each() 메서드는 매개변수로 입력한 함수로 for in 반복문처럼 객체나 배열의 요소를 검사하는 메서드이다.  

1. $.each(object, function(index, item){})
2. $(selector).each(function(index,item){})

> $.each() 메서드 사용법  
자바스크립트 배열에 들어있는 내용을 HTML 페이지에 표시하는 간단한 예제

```javascript
$(document).ready(function () {
    var array = [
        {name : "sskim", link : "www.sskim.com"},
        {name : "google", link : "www.google.com"},
        {name : "naver", link : "www.naver.com"}
    ];

    $.each(array, function (index, item) {

        var output = "";

        output += '<a href="' + item.link + '">';
        output += ' <h1>' + item.name + '</h1>';
        output += '</a>';

        document.body.innerHTML += (output);
    });
});
```  


- - -
> jQuery 배열 관리
jQuery의 배열 객체는 따로 만드는 것이 아니라, 선택자로 여러 개의 문서 객체를 선택할 때 생성 된다.

예제
```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .high-light-0 {  background: yellow;  }
        .high-light-1 {  background: orange;  }
        .high-light-2 {  background: blue;  }
        .high-light-3 {  background: green;  }
        .high-light-4 {  background: red;  }
    </style>
</head>
<body>
<script src="../jquery-3.2.1.js"></script>
<script>
    $(document).ready(function () {
        $("h1").addClass('high-light');

        $("h1").each(function (index, item) {
            //$(item).addClass('high-light-' + index);
            $(this).addClass('high-light-' + index);
            //이렇게 매개변수 item을 사용할 수도 있지만 일반적으로 this키워드를 더 많이 사용한다.
        });
    });
</script>

<h1>item - 0</h1>
<h1>item - 1</h1>
<h1>item - 2</h1>
<h1>item - 3</h1>
<h1>item - 4</h1>
</body>
</html>
```