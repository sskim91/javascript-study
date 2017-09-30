# 8.9 ECMAScript5 String 객체

ECMA5Script5 에서 String 객체의 다음 메서드가 추가 되었다.

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| trim() | 문자열 양쪽 끝의 공백을 제거 |

```javascript
var text = "  text  ";

var output = "";
output += "++" + text + "++\n";
output += "++" + text.trim() + "++";
alert(output);
```