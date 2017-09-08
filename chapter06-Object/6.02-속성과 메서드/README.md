## 속성과 메서드

> 배열 내부에 있는 값을 *요소(element)* 라고 한다.  
반면 객체 내부에 있는 값은 *속성(property)* 라고 한다.

배열의 요소와 마찬가지로 객체의 속성 코드도 모든 형태의 자료형을 가질 수 있다.
```javascript
var object = {
        number: 273,
        string: "retina",
        boolean : true,
        array : [52,273,103,32],
        method : function () {
            
        }
};
````
> 객체의 속성 중 함수 자료형인 속성을 *메서드(method)* 라고 부른다.

person 객체는 name 속성과 eat 속성이 있으며, eat 속성은 함수 자료형이다.
```javascript
//속성과 메서드의 구분
var person = {
    name: "떱떱",
    eat: function (food) {
        alert(this.name + "이" + food + "먹는다.");
    }
};

//메서드 호출
person.eat("음료수");
````  

> 자기 자신이 가진 속성을 출력하고 싶을 때는 자기 자신이 가진 속성임을 분명하게 표시하는  
this 라는 키워드를 사용해야 한다.
