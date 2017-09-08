## 7.2 프로토 타입 (prototype)

> 속성은 모든 객체가 다른 값을 갖지만 메서드는 모두 같은 값을 갖는다.  
객체를 생성할 때 마다 동일한 함수를 계속 생성함으로써 비효율적이다.  
그래서 사용하는 것이 프로토타입 이다.  
*프로토타입은 생성자 함수로 생성된 객체가 공통으로 가지는 공간이다.*  

프로토 타입으로 메서드 생성
```javascript
function Student(name, korean, math, english, science) {
        this.이름 = name;
        this.국어 = korean;
        this.수학 = math;
        this.영어 = english;
        this.과학 = science;
    }  
    
    //프로토타입
    Student.prototype.getSum = function () {
        return this.국어 + this.수학 + this.영어 + this.과학;
    };   
    

    Student.prototype.getAverage = function () {
        return this.getSum() / 4;
    };  

    Student.prototype.toString = function () {
        return this.이름 + '\t' + this.getSum() + '\t' + this.getAverage();
    };  
    

    var students = [];
    students.push(new Student("sskim", 95, 95, 94, 93));
    students.push(new Student("sskim", 90, 90, 93, 88));  
    

    //출력
    var output = '이름\t총점\t평균\n';
    for (var i in students) {
        output += students[i].toString() + '\n';
    }
    alert(output);
```

