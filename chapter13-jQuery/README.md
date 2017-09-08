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
반면 jQuery의 이벤트 메서드는 표준 이벤트 모델이나 인터넷 익스플로러 이벤트 모델과 마찬가지로 이벤트로 여러 개의 함수를 연결할 수 있다.

