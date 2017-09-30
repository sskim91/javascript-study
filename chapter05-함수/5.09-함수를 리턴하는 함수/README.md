# 함수를 리턴하는 함수

예제

```javascript
//익명 함수를 리턴하는 함수
function returnFunction() {
    return function () {
        alert("Hello Function");
    }
}

//함수를 호출
returnFunction();
```

함수를 리턴하는 함수를 사용하는 가장 큰 이유는 **클로저(closure)** 때문이다.