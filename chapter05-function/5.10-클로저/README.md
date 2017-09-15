# 클로저(closure)

지역변수의 유효 범위

```javascript
function test(name) {
  var output = "hello"+name;
}

alert(output);
```

함수 안에 있는 변수는 지역 변수이므로 함수 외부에서는 사용할 수 없다.  
그러나 클로저를 사용하면 이 규칙을 위반할 수 있다.

클로저 1
```javascript
function test(name) {
  var output = "hello"+name;
  return function() {
    alert(output);
  };
  
  test("sskim");
}
```

위의 코드 지역변수 output은 함수가 종료될 때 사라져야 하지만  
해당 변수가 이후에도 활용될 가능성이 있으므로 자바스크립트는 변수를 제거하지 않고 남겨둔다.

클로저에 대한 자세한 설명이 나와있는 링크  
[MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Closures)  
[자바스크립트 클로저 쉽게 이해하기](http://chanlee.github.io/2013/12/10/understand-javascript-closure/)  


