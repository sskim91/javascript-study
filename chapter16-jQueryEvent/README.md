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
위의 코드는 마우스가 진입하면 reverse 클래스 속성을 추가하고, 마우스가 빠져나가면 reverse 클래스 속성을 제거한다.

## 16.3 간단한 이벤트 연결

간단한 방식으로 연결할 수 있는 이벤트 표
<pre>
blur      |   focus       |   focusin   |   focusout  |   load
resise    |   scroll      |   unload    |   click     |   dblclick
mousedown |   mouseup     |   mousemove |   mouseover |   mouseout
mouseenter|   mouseleave  |   change    |   select    |   submit
keydown   |   keypress    |   keyup     |   error     |   ready
</pre>

간단한 방식으로 이벤트를 연결할 때는 아래와 같은 방법을 사용한다.
```javascript
$(selector).method(function(event){});
```

이벤트 연결 메서드
hover() 메서드
| 메서드 이름 | 설명 |
| :------------- | :------------- |
| hover() | mouseenter 이벤트와 mouseleave 이벤트를 동시에 연결한다. |

```javascript
$(selector).hover(function(event){}, function(event){});
```

보통 hover() 메서드를 이용해서 메뉴의 드롭바를 구현한다.