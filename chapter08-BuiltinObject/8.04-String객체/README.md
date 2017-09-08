# 8.4 String 객체

기본 속성과 메서드

| 속성 이름     | 설명     |
| :------------- | :------------- |
| length       | 문자열의 길이를 나타낸다.     |


| 메서드 이름 | 설명 |
| :------------------ | :------------- |
| charAt(position) | position에 위치하는 문자를 리턴 |
| charCode(position) |  position에 위치하는 문자의 유니코드 번호를 리턴 |
| concat(args)  | 매개변수로 입력한 문자열을 이어서 리턴 |
| indexOf(searchString, position) | 앞에서부터 일치하는 문자열의 위치를 리턴 |
| lastIndexOf(searchString, position) | 뒤에서부터 일치하는 문자열의 위치를 리턴 |
| match(regExp) | 문자열 안에 regExp가 있는지 확인 |
| replace(regExp, replacement) | regExp를 replacement로 바꾼 뒤 리턴 |
| search(regExp) |  regExp와 일치하는 문자열의 위치를 리턴 |
| slice(start, end) | 특정 위치의 문자열을 추출해 리턴 |
| split(seperator, limit) | separator로 문자열을 잘라서 배열을 리턴 |
| substr(start, count) | start부터 count만큼 문자열을 잘라서 리턴 |
| substring(start, end) | start부터 end까지 문자열을 잘라서 리턴 |
| toLowerCase() | 문자열을 소문자로 바꾸어 리턴 |
| toUpperCase() | 문자열을 대문자로 바꾸어 리턴 |

잘못된 String 객체의 메서드 사용
```javascript
var string = "abcde";  

string.toUpperCase();
alert(string);
```

String 객체의 메서드는 자기 자신을 변화시키지 않고 리턴한다.

올바른 String 객체의 메서드 사용
```javascript
var string = "abcde";  

string = string.toUpperCase();
alert(string);
```