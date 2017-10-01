# jQuery

jQuery를 사용한 모든 웹 페이지는 다음 코드로 시작한다.

```javascript
<script>
  $(document).reday(function(){

  });
</script>
```

$(document).ready() 는 문서가 준비되면 매개변수로넣은 콜백 함수를 실행하라는 의미이다.  

아래의 메서드와 비슷한 기능을 수행한다.

```javascript
<script>
  window.onload = function(){
    
  };
</script>
```

그러나 고전 이벤트 모델은 한번의 하나의 이벤트만 연결할 수 있다.  
반면 jQuery의 이벤트 메서드는 표준 이벤트 모델이나   
인터넷 익스플로러 이벤트 모델과 마찬가지로 이벤트로 여러 개의 함수를 연결할 수 있다.

- - -

### CSS 선택자 정리

css의 가장 기본적인 선택자는 전체 선택자 

```javascript
<script>
    $(document).reday(function(){
        $('*').css("color", "red");
        전체 선택시 * 를 사용
    });
</script>
```

**태그 선택자**<br>  
태그 선택자는 특정한 태그를 선택하는 선택자로 태그의 이름을 그냥 사용한다.

```javascript
<script>
    $(document).reday(function(){
        $("h1").css("color", "oragne");
    });
</script>
```

**아이디 선택자**<br>  
아이디 선택자는 특정한 id 속성이 있는 문서 객체를 선택하는 선택자이다.

```html
<body>
    <h1 id="target">h1 tag</h1>
</body>
```

```javascript
<script>
    $(document).reday(function(){
        //아이디 선택자는 #을 이용해 사용한다.
        $("#target").css("color", "red");
    });
</script>
```

**클래스 선택자**<br>
클래스 선택자는 특정한 class 속성이 있는 문서 객체를 선택하는 선택자이다.

```html
<body>
    <h1 class="item">h1 tag</h1>
</body>
```

```javascript
<script>
    $(document).reday(function(){
        //클래스 선택자는 .을 이용해 사용한다.
        $(".itme").css("color","red");
    });
</script>
```