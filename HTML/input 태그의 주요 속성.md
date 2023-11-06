#### 1. 자동으로 입력 커서를 갖다 놓는 autofocus 속성

``` html
<input type=텍스트-입력-필드 autofocus required>
```

autofocus 속성을 사용하면 페이지를 불러오자마자 폼에서 원하는 요소에 마우스 포인터를 표시할 수 있다.


#### 2. 힌트를 표시해 주는 placeholder 속성

![[22.png]]
``` html
<li>
	<label for="phone">연락처</label>
	<input type="tel" id="phone" placeholder="하이픈 빼고 입력해 주세요.(01012345678)" required>
</li>
```

이런식으로 힌트 내용을 표시해주는 속성이다


#### 3. 읽기 전용 필드를 만들어 주는 readonly 속성

``` html
<input type=텍스트-입력-필드 readonly>
```

사용자가 입력하지는 못하고 읽게만 하는 읽기 전용 필드


#### 4. 필수 입력 필드를 지정하는 required 속성

필수 필드에 필요한 내용이 모두 채워졌는지 검사해야 하는데, 반드시 입력해야 하는 내용에는 required 속성을 지정해 필수 필드로 만들 수 있다.

ex)
``` html
<form>
    <fieldset>
      <legend>배송 정보</legend>
      <ul id="shipping">
        <li>
          <label for="prod">주문 상품</label>
          <input type="text" id="prod" value="상품용 3KG" readonly>
        </li>
        <li>
          <label for="user-name">이름 </label>
          <input type="text" id="user-name" autofocus required>
        </li>
        <li>
          <label for="addr">배송 주소</label>
          <input type="text" id="addr" required>
        </li>
        <li>
          <label for="mail">이메일</label>
          <input type="email" id="mail">
        </li>        
        <li>
          <label for="phone">연락처</label>
          <input type="tel" id="phone" placeholder="하이픈 빼고 입력해 주세요.(01012345678)" required>
        </li>
        <li>
          <label for="d-day">배송 지정</label>
          <input type="date" id="d-day"> <small>(주문일로부터 최소 3일 이후)</small>
        </li>        
      </ul>  
    </fieldset>
    <div>
      <input type="submit" value="주문하기">
      <input type="reset" value="취소하기">
    </div>        
</form>
```