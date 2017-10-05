## 필터 선택자

```diff
+선택자 중에 : 기호를 포함하는 선택자를 필터 선택자라고 한다.
```

jQuery의 입력 양식 필터 선택자

| 선택자 형태 | 설명 |
| :------------- | :------------- |
| 요쇼:button | input 태그 중 type 속성이 button인 문서 객체와 button 태그를 선택  |
| 요소:checkbox | input 태그 중 type 속성이 check인 문서 객체를 선택  |
| 요소:file | input 태그 중 type 속성이 file인 문서 객체를 선택 |
| 요소:image | input 태그 중 type 속성이 image인 문서 객체를 선택 |
| 요소:password | input 태그 중 type 속성이 password인 문서 객체를 선택 |
| 요소:radio  | input 태그 중 type 속성이 radio인 문서 객체를 선택  |
| 요소:reset  | input 태그 중 type 속성이 reset인 문서 객체를 선택  |
| 요소:submit | input 태그 중 type 속성이 submit인 문서 객체를 선택 |
| 요소:text | input 태그 중 type 속성이 text인 문서 객체를 선택 |

jQuery의 입력 양식 필터 선택자 2

| 선택자 형태 | 설명 |
| :------------- | :------------- |
| 요소:checked | 체크되어 있는 입력 양식을 선택 |
| 요소:disabled | 비활성화된 입력 양식을 선택 |
| 요소:enabled | 활성화된 입력 양식을 선택 |
| 요소:focus |  초점이 맞추어져 있는 입력 양식을 선택 |
| 요소:input |  모든 입력 양식을 선택 (input, textarea, select, button 태그) |
| 요소:selected | option 객체 중 선택된 태그를 선택  |

예제

```javascript
<body>
<select name="" id="">
	<option value="a">a</option>
	<option value="b">b</option>
	<option value="c">c</option>
	<option value="d">d</option>
	<option value="e">e</option>
</select>
<script>
	$(document).ready(function(){
	   //3초 후에 코드를 실행
        setTimeout(function () {
            var value = $("select > option:selected").val();

            alert(value);
        }, 3000);
	});
</script>
</body>
```

## 위치 필터 선택자

jQuery 위치 필터 선택자

| 선택자 형태 | 설명 |
| :------------- | :------------- |
| 요소:odd | 홀수 번째에 위치한 문서 객체를 선택 |
|	요소:even |	짝수 번째에 위치한 문서 객체를 선택	|
|	요소:first | 첫 번째에 위치한 문서 객체를 선택	|
|	요소:last	|	마지막에 위치한 문서 객체를 선택	|

## 함수 필터 선택자

jQuery의 함수 필터 선택자

| 선택자 형태 | 설명 |
| :------------- | :------------- |
| 요소:contain | 특정 문자열을 포함하는 문서 객체를 선택 |
|	요소:eq(n)	|	n번째에 위치하는 문서 객체를 선택 	|
|	요소:gt(n)	|	n번째 초과에 위치하는 문서 객체를 선택	|
|	요소:has(h1)	| h1 태그가 있는 문서 객체를 선택	|
|	요소:lt(n)	|	n번째 미만에 위치하는 문서 객체를 선택	|
|	요소:not(선택자)	|	선택자와 일치하지 않는 문서 객체를 선택	|
|	요소:nth-child(3n+1) | 3n+1번째에 위치하는 문서 객체를 선택(1,4,7...)|
