# 14.1 기본 필터 메서드

jQuery의 선택자를 사용하면 원하는 문서 객체를 대부분 선택할 수 있다.  
기본적으로 지원하지 않는 필터로 문서 객체를 선택해야 한다면 filter() 메서드를 사용해야 한다.

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| filter() | 문서 객체를 필터링 |

filter() 메서드는 다음 두 가지 형태로 사용한다.

1. $(selector).filter(selector);
2. $(selector).filter(function(){});

filter() 메서드의 매개변수에 선택자를 입력 예제

```javascript
$(document).ready(function () {
    $("h3").filter(":even").css({
            backgroundColor: "blue",
            color: "white"
        });
});
```

filter() 메서드의 매개변수에 함수를 넣는 예제  
이때 입력하는 함수는 매개변수로 index를 갖는다.  
함수에서 리턴하는 값에 따라 문서 객체를 선택한다.

```javascript
$(document).ready(function () {
    $("h3").filter(function (index) {
        return index % 3 == 0;
    }).css({
        backgroundColor: "blue",
        color: "white"
    });
});
```

filter() 메서드의 매개변수에 선택자를 입력한 예제를 메서드 체이닝을 사용해 한줄로 나타내기

```javascript
$(document).ready(function () {
        $("h3").css("background", "orange").filter(":even").css("color", "red");
    });
```

체이닝을 사용하면 코드가 간결해지지만 이 방법은 문서 객체의 범위를 점점 좁게만 선택할 수 있게 된다. 아래의 코드를 체이닝 하려면 지금까지 배운 방법으로는 체이닝을 사용하는 형태로 바꿀수 없다. 체이닝을 사용할 때 추가한 filter() 메서드를 제거하려면 end() 메서드를 사용해야 한다.

```Javascript
$(document).ready(function(){
  $("h1").css("background", "orange");
  $("h1:even").css("color", "white");
  $("h1:odd").css("color", "red");
});
```

문서 객체 탐색 종료 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| end() | 문서 객체 선택을 한 단계 뒤로 돌린다. |

end() 메서드를 사용한 체이닝

```javascript
$("h1").css("background", "orange").filter(":even").css("color", "white").end().filter(":odd").css("color", "red");
```
