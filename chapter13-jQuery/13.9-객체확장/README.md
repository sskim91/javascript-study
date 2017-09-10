## 13.9 객체확장

기존의 자바스크립트의 객체에 새 속성을 추가할 때 사용한다.<br>
적은 개수의 속성이라면 문제가 없으나 많은 수의 속성을 추가할 때 유용하다.<br>

> $.extend() 메서드 사용법

```javascript
$.extend(object, addObject, addObjec..)
```

```javascript
$(document).ready(function () {
    var object = {
        name : "sskim"
    };

    //$.extend()
    $.extend(object, {
        region: "seoul",
        gender : "male"
    });

    var output = "";
    $.each(object, function (index, item) {
        output += index + " : " + item + "\n";
    });
    alert(output);
});
```