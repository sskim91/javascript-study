## 이벤트 강제 발생

jQuery에서는 이벤트를 강제로 발생시킬 때는 trigger() 메서드를 사용한다.

| 메서드 이름 | 설명 |
| :------------- | :------------- |
| trigger() | 이벤트를 강제로 발생시킨다. |

trigger() 메서드는 다음과 같은 형태로 사용한다.

<pre>
  1. $(selector).trigger(eventName)
  2. $(selector).trigger(eventName, data)
</pre>
