# 자바스크립트 내장 함수

### 타이머 함수

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| setTimeOut(function, millisecond) | 일정 시간 후 함수를 한번 실행 |
| setInterval(function, millisecond) | 일정 시간마다 함수를 반복해서 실행 |
| clearTimeout(id) | 일정 시간 후 함수를 한번 실행하는 것을 중지 |
| clearInterval(id) | 일정 시간 마다 함수를 반복하는 것을 중단 |

**차이점**
> setTimeout() 메서드는 특정한 시간 후에 함수를 한번 실행  
setInterval() 메서드는 특정한 시간마다 함수를 실행

```javascript
<script>
    setTimeout(function () {
        alert("3초");
    }, 3000);
</script>
```

setTimeout() 함수의 경우 한번만 실행 하므로 주의할 사항이 없지만  
setInterval() 함수의 경우 지속적으로 실행하게되므로 타이머를 멈춰야할 필요가 있다.  
이때 clearTimeout()과 clearInterval() 함수를 사용한다.

```javascript
<script>

    var intervalId = setInterval(function () {
        alert("hi");
    },1000);

    setTimeout(function () {
        //타이머를 종료
        clearInterval(intervalId);
    }, 3000);
</script>
```

setTimeOut() 함수와 setInterval() 함수를 사용하면 타이머 아이디를 리턴하는데
이 타이머 아이디를 clearTimeout()함수와 clearInterval() 함수에 매개변수에 넣어주면 타이머를 정지할 수 있다.

---
### 코드 실행 함수

| 함수 이름 | 설명 |
| :------------- | :------------- |
| eval(string) | string을 자바스크립트 코드로 실행 |

eval() 함수는 문자열을 자바스크립트 코드로 실행하는 함수이다.

### 숫자 확인 함수

| 함수 이름 | 설명 |
| :------------- | :------------- |
| isFinite() | number가 무한한 값인지 확인 |
| isNaN() | number가 NaN인지 확인 |

### 숫자 변환 함수

| 함수 이름 | 설명 |
| :------------- | :------------- |
| parseInt(string) | string을 정수로 바꾸어준다 |
| parseFloat(string)  | string을 유리수로 바꾸어준다 |