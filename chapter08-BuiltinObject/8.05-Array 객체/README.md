## 8.5 Array 객체

| 생성자 함수 | 설명 |
| :------------- | :------------- |
| Array() | 빈 배열을 만든다. |
| Array(number) | 매개변수만큼의 크기를 가지는 배열을 만든다. |
| Array(any, ..., any) | 매개변수를 배열로 만든다. |

```javascript
var arr1 = [52, 33, 12, 56, 76];
var arr2 = new Array();
var arr3 = new Array(10);
var arr4 = new Array(12, 13, 14, 15, 16);
```

속성과 메서드  

| 속성 이름 | 설명 |
| :------------- | :------------- |
| length | 요소의 개수를 알아낸다. |

```javascript
var array = ['A', 'B', 'C', 'D'];  

var output = "";  

for (var i=0; i<array.length; i++) {
    output += i + " : " + array[i] + "\n";
}

alert(output);
```
Array 객체의 메서드  

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| concat() | 매개변수로 입력한 배열의 요소를 모두 합쳐 배열을 만들어 리턴 |
| join()  | 배열 안의 모든 요소를 문자열로 만들어 리턴  |
| pop()* |  배열의 마지막 요소를 제거하고 리턴 |
| push()* | 배열의 마지막 부분에 새로운 요소를 추가 |
| reverse()*  | 배열의 요소 순서를 뒤집는다. |
| slice() | 요소의 지정한 부분을 리턴 |
| sort()* | 배열의 요소를 정렬 |
| splice()* | 요소의 지정한 부분을 삭제하고 삭제한 요소를 리턴 |

> *표시된 메서드는 자기 자신을 변화시킨다.

---  

Array 정렬

Array 객체의 sort() 메서드의 정렬 방법에 변화를 주고 싶을 때는 sort() 메서드의 매개변수로 함수를 넣어준다. sort() 메서드의 매개변수로 넣는 함수는 기본적으로 다음과 같이 매개변수 두 개를 받을 수 있어야 한다.
```javascript
array.sort(function(left, right){

});
```
**오름차순 정렬**
```javascript
function (left, right) {
  return left - right;
}
```
**내림차순 정렬**
```javascript
function (left, right) {
  return right - left;
}
```