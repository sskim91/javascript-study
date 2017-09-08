## 7.1 생성자 함수

> 자바스크립트 함수를 만들어서 new 키워드로 객체를 생성한다.

```javascript
function Student() {
  
}

var student = new Student();
```

>  함수를 이용하여 생성한 객체의 속성값과 메소드를 정의하기 위해서는   
**this** 키워드를 사용하면 된다.  

```javascript
function Student(name, korean, math, english, science) {
        this.이름 = name;
        this.국어 = korean;
        this.수학 = math;
        this.영어 = english;
        this.과학 = science;   
    }
```

> 생성자 함수 안에 메서드를 만드는 방법

```javascript
function Student(name, korean, math, english, science) {
        this.이름 = name;
        this.국어 = korean;
        this.수학 = math;
        this.영어 = english;
        this.과학 = science;  
        

       this.getSum = function () {
            return this.국어 + this.수학 + this.영어 + this.과학;
        }  
        

        this.getAverage = function () {
            return this.getSum() / 4;
        };  
      

        this.toString = function () {
            return this.이름 + '\t' + this.getSum() + '\t' + this.getAverage();
        };
    }
    
    var student = new Student("sskim",90,95,94,90);
```

> Student() 함수는 new 키워드로 객체를 생성하므로 생성자 함수이다.  
Student 생성자 함수로 만든 객체 student를 객체 또는 인스턴스라고 한다.
