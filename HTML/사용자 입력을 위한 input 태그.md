``` html
<input type = "type 속성">
```
`<input>` 태그는 다양한 폼에서 사용자가 입력한 정보를 받을 때 사용한다는 것을 잘 기억해 두자 

#### type 속성

|  속성값                                                                 | 설명  |                                                                      |                                                                                   |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| [button](http://tcpschool.com/html-input-types/intro)                  | 클릭할 수 있는 버튼을 정의함.                                                     |
| [checkbox](http://tcpschool.com/html-input-types/checkbox)             | 체크박스(checkbox)를 정의함.                                                      |
| [color](http://tcpschool.com/html-input-types/color)                   | 색을 선택할 수 있는 입력 필드(color picker)를 정의함.                             |
| [date](http://tcpschool.com/html-input-types/date)                     | 날짜를 선택할 수 있는 입력 필드를 정의함. (year, month, day)                      |
| [datetime-local](http://tcpschool.com/html-input-types/datetime-local) | 날짜와 시간을 선택할 수 있는 입력 필드를 정의함. (year, month, day, hour, minute) |
| [email](http://tcpschool.com/html-input-types/email)                   | 이메일 주소를 입력할 수 있는 입력 필드를 정의함.                                  |
| [file](http://tcpschool.com/html-input-types/file)                     | 업로드할 파일을 선택할 수 있는 입력 필드와 “파일 선택” 버튼을 정의함.             |
| [hidden](http://tcpschool.com/html-input-types/hidden)                 | 사용자에게는 보이지 않는 숨겨진 입력 필드를 정의함.                               |
| [image](http://tcpschool.com/html-input-types/image)                   | 제출 버튼(submit button)으로 사용될 이미지를 정의함.                              |
| [month](http://tcpschool.com/html-input-types/month)                   | 날짜를 선택할 수 있는 입력 필드를 정의함. (year, month)                           |
| [number](http://tcpschool.com/html-input-types/number)                 | 숫자를 입력할 수 있는 입력 필드를 정의함.                                         |
| [password](http://tcpschool.com/html-input-types/password)             | 비밀번호를 입력할 수 있는 입력 필드를 정의함.                                     |
| [radio](http://tcpschool.com/html-input-types/radio)                   | 라디오 버튼(radio button)을 정의함.                                               |
| [range](http://tcpschool.com/html-input-types/range)                   | 슬라이드 바를 조정하여 범위 내의 숫자를 선택할 수 있는 입력 필드를 정의함.        |
| [reset](http://tcpschool.com/html-input-types/reset)                   | 리셋 버튼(reset button)을 정의함.                                                 |
| [search](http://tcpschool.com/html-input-types/search)                 | 검색어를 입력할 수 있는 텍스트 필드를 정의함.                                     |
| [submit](http://tcpschool.com/html-input-types/submit)                 | 제출 버튼(submit button)을 정의함.                                                |
| [tel](http://tcpschool.com/html-input-types/tel)                       | 전화번호를 입력할 수 있는 입력 필드를 정의함.                                     |
| [text](http://tcpschool.com/html-input-types/text)                     | type 속성의 기본값으로, 한 줄로 된 텍스트 필드를 정의함.                          |
| [time](http://tcpschool.com/html-input-types/time)                     | 시간을 선택할 수 있는 입력 필드를 정의함. (hour, minute)                          |
| [url](http://tcpschool.com/html-input-types/url)                       | URL 주소를 입력할 수 있는 입력 필드를 정의함.                                     |
| [week](http://tcpschool.com/html-input-types/week)                     | 날짜를 선택할 수 있는 입력 필드를 정의함. (year, week)                            |

1. type="text"와 type="password"
``` html
<input type="text">
<input type="password">

ex)
<form>
	<fieldset>
		<label>아이디:<input type="text" id="user_id" size="10"></label>
		<label>비밀번호:<input type="password" id="user_id" size="10"><label>
		<input type="submit" value="로그인">
	</fieldset>
</form>
```

![[12.png]]

2. 체크 박스와 라디오 버튼
``` html
<input type="checkbox">
<input type="radio">
```

![[14.png]]

3. 숫자 입력 필드를 나타내는 type="number", type="range"
``` html
<input type="number">
<input type="range">
```

![[16.png]]

ex) [[체크박스, 라디오, 숫자입력 필드 예제]]


4. 날짜 입력을 나타내는 type="date", type="month", type="week" 
``` html
<input type="date | month | week">

ex)
<input type="date">
<input type="month">
<input type="week">
```

![[17.jpg]]

5. 시간 입력을 나타내는 type="time", type="datetime", type="datetime-local"
``` html
<input type="time | datetime | datetime-local">
```

![[18.png]]

6. 전송, 리셋 버튼을 나타내는 type="submit", type="reset"
``` html
<input type="submit | reset" value="버튼에 표시할 내용">
```

전송 버튼을 나타내는 submit은 폼에 입력한 정보를 서버로 전송한다.

7. 이미지 버튼을 나타내는 type="image"
``` html
<input type="image" src="이미지 경로" alt="대체 텍스트">
```

8. 기본 버튼을 나타내는 type="button"
``` html
<input type="button" value="버튼에 표시할 내용">
```

ex) [[버튼 예제]]

9. 파일을 첨부할 때 사용하는 type="file"
``` html
<input type="file">
```

10. 히든 필드 만들 때 사용하는 tpye="hidden"
``` html
<input type="hidden" name="이름" value="서버로 넘길 값">
```
화면의 폼에는 보이지 않지만 사용자가 입력을 마치면 폼과 함께 서버로 전송되는 요소
사용자에게 굳이 보여 줄 필요는 없지만 관리자는 알아야 하는 정보는 히든 필드로 입력함

ex) [[히든 필드 예제]]
