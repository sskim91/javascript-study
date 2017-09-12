# 8.10 JSON 객체

JSON(Javascript Object Notation)은 자바스크립트 객체의 형태를 갖는 문자열을 뜻한다.

ECMAScript5 JSON 객체의 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| JSON.stringify() | 자바스크립트 객체를 JSON 문자열로 변환 |
| JSON.parse()  | JSON 문자열을 자바스크립트 객체로 변환 |

자바스크립트 객체를 JSON 문자열로 변환
JSON.stringify() 예제
```javascript
var object = {
     name: "sskim",
     gender: "male"
 };

alert(JSON.stringify(object));
```

JSON 문자열을 자바스크립트 객체로 바꾸는 역할
JSON.parse() 예제
```javascript
var object = {
    name: "sskim",
    gender: "male"
};

var copy = JSON.parse(JSON.stringify(object));
alert(copy.name + " : " + copy.gender);
```
