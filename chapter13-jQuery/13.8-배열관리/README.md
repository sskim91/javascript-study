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
