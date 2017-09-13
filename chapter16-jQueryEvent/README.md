# 16 이벤트

jQuery로 이벤트를 연결하는 가장 기본적인 방법은 on() 메서드를 사용하는 것이다.

이벤트 연결 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| on() | 이벤트를 연결한다. |

on() 메서드는 두 가지 형태로 사용할 수 있다.

1. $(selector).on(eventName, function(event){})
2. $(selector).on(object)

on() 메서드 첫번째 형태

```javascript
<body>
  <h1>Header-0</h1>
  <h1>Header-1</h1>
  <h1>Header-2</h1>
</body>  

<script>
  $(document).ready(function(){
    //이벤트를 연결
    $("h1").on("click", function(){
        $(this).html(function(index, html){
            return html + "+";
        });
    });
  });
</script>
```
위 코드는 h1 태그를 click 이벤트에 연결하고 이벤트 발생 시 이벤트 발생 객체에 '+' 글자를 추가한다.

on() 메서드 두번째 형태
on() 메서드의 매개변수에 객체를 넣어준다.
```javascript
$(document).ready(function(){
    //이벤트를 연결
    $("h1").on("click", function(){
        $(this).html(function(index, html){
            return html + "+";
        });
    });

    $("h1").on({
      mouseenter : function () {$(this).addClass("reverse");},
      mouseleave :function () {$(this).removeClass("reverse");}
    });
});
```
