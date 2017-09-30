# 매개변수와 리턴 값

매개변수와 리턴 값을 갖는 함수를 만드는 방법

```javascript
function 함수이름(매개변수...) {
  함수 코드
  return 리턴 값;
}
```

매개 변수에 따라서 여러 결과가 나오는 Javascript의 **Array()** 함수

함수 형태 | 설명 
---------- | ---------- 
Array() | 빈 배열을 만듭니다.
Array(number) | 매개변수 값만큼의 크기를 갖는 배열을 만듭니다.
Array(매개변수..,매개변수) | 매개변수를 배열로 만듭니다.


## 가변인자 함수

가변 인자 함수는 매개변수의 개수가 변할 수 있는 함수이다.  

**자바스크립트의 모든 함수는 내부에 기본적으로 변수 *arguments*가 있다.**

arguments 객체를 사용한 가변 인자 함수

```javascript
//arguments 객체를 사용한 가변 인자 함수
function sumAll() {
    var output = 0;
    for (var i=0; i<arguments.length; i++) {
        output += arguments[i];
    }
    return output;
}

alert(sumAll(1, 2, 3, 4, 5, 6, 7, 8, 9, 10));

```
