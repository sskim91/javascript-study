## 8.6 Date 객체

Date 객체를 생성 하는 방법
```javascript
//현재 시각
var date = new Date();
alert(date);
```

문자열을 사용한 Date 객체 생성
```javascript
//문자열을 사용한 Date 객체 생성
var date = new Date("December 25, 1991");
var date = new Date("December 25, 1991 09:00:23")
alert(date);
```

숫자를 사용한 Date 객체 생성
연, 월-1, 일, 시, 분, 초, 밀리 초 순서
```javascript
//숫자를 사용한 Date 객체 생성
var date = new Date(1991, 12, 25);
var date = new Date(1991, 12, 25, 24, 23);
var date = new Date(1991, 12, 25, 24, 23, 1);
```

#### Date 객체 메서드

일주일 후의 시간 구하기
```javascript
var date = new Date();

date.setDate(date.getDate() + 7);
```

###### 시간 간격 계산 방법
```javascript
var now = new Date();
var beofre = new Date('December 25, 1991');

var interval = now.getDate() - beofre.getDate();
interval = Math.floor(interval / (1000 * 60 * 60 * 24));

alert("Interval: " + interval + "일");
```
