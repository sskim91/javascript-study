# 8.8 ECMAScript5 Array 객체

#### 확인 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| Array.isArray() | 배열인지 확인 |

#### ECMAScript 5 Array 객체의 탐색 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| indexOf() | 특정 요소를 앞쪽부터 검색 |
| lastIndexOf() | 특정 요소를 뒤쪽부터 검색 |

indexOf() 메서드와 lastIndexOf() 메서드 모두 매개변수에 검색하려는 객체를 입력  
만약 내부에 검색하려는 객체가 있으면 해당 객체가 위치하는 인덱스를 리턴하고 없으면 -1을 리턴한다.

#### 반복 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| forEach() | 배열 각각의 요소를 사용해 특정 함수를 for in 반복문처럼 실행 |
| map() | 기존의 배열에 특정 규칙을 적용해 새로운 배열을 만든다. |


forEach() 메서드 예제

```javascript
var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

var sum = 0;
var output = "";  

array.forEach(function (element, index, array) {
    sum += element;
    output += index + ": " + element + "->" + sum + "\n";
});  

alert(output);
```

map() 메서드는 배열의 각 요소를 변경해 새로운 배열을 리턴하는 메서드  
map() 메서드 예제

```javascript
var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

var output = array.map(function (element) {
    return element * element;
});

alert(output);
```


#### 조건 메서드

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| filter() | 특정 조건을 만족하는 요소를 추출해 새로운 배열을 만든다. |
| every() | 배열의 요소가 특정 조건을 모두 만족하는지 확인 |
| some()  | 배열의 요소가 특정 조건을 적어도 하나 만족하는지 확인 |

filter() 메서드의 매개변수로 입력한 함수는 불 자료형 값으로 리턴해야 한다.  
이때 리턴하는 값이 true인 배열의 요소만을 골라 새로운 배열을 만든다.ㄴ

filter() 메서드 예제
```javascript
var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

array = array.filter(function (element, index, array) {
    return element <= 5;
});
```
