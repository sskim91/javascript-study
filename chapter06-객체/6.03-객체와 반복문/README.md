## 6.3 객체와 반복문

    - 배열은 단순 for 반복문과 for in 반복문으로 쉽게 접근할 수 있다.
    - but 객체는 단순 for 반복문으로 객체의 속성을 살펴보는 것은 불가능하다.
    - 객체의 속성을 모두 살펴보려면 for in 반복문을 사용해야 한다.
    
```javascript  
var product = {
    name: "하이하이",
    age: 27,
    sex: "male",
    location: "seoul"
};  

var output = "";

for (var key in product) {
    output += key + " : " + product[key] + "\n";
}  

alert(output);
```