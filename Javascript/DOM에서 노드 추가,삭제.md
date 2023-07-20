# 노드 리스트란

```html
<h1>Web Programming</h1>
<ul id = "itemList">
    <li>HTML</li>
    <li>CSS</li>
    <li>Javascript</li>
</ul>
```

이때 콘솔 창에 document.querySelectorAll("li")라고 하면 현재 문서에서 li요소를 모두 가져오기 때문에 노드 리스트가 반환된다.

만약 어떠한 태그를 노드로 추가한다면 단순히 태그에 해당하는 요소 노드뿐만 아니라 텍스트 노드와 속성 노드로 추가해야 한다.

<br>

# 텍스트 노드를 사용하는 새로운 요소 추가하기

1. 요소 노드 만들기
   
   `document.createElement(노드명)` 이렇게 새로운 요소 노드를 만든다
   
   ex) `var newP = document.createElement("p");` : 이렇게 하면 새로운 p요소가 만들어진다.
   
   ![](C:\Users\luili\Desktop\coding_study\Do_it_web\image\image_21.jpg)

2. 텍스트 노드 만들기
   
   `document.createTextNode(텍스트);` 
   
   ex ) `var txtNode = document.createTextNode("이건 텍스트입니다");`
   
   ![](C:\Users\luili\Desktop\coding_study\Do_it_web\image\image_22.jpg)

3. 자식 노드 연결하기
   
   `부모노드.appendChild(자식노드)` : 요소 노드들을 연결할 때 사용한다. 이 메서드를 이용해서 연결하는 노드는 자식 노드 중 맨 끝에 추가된다.
   
   ex) 
   
   ```javascript
   newP.appendChild(txtNode);
   document.getElementById("info").appendChild(newP);
   ```
   
   ![](C:\Users\luili\Desktop\coding_study\Do_it_web\image\image_23.jpg)

전체 소스 코드 예시는 다음과 같다.

```html
(...)
<div id="container">
  <h1>DOM을 공부하자</h1>
  <a href="#" onclick="addP(); this.onclick='';">더 보기</a>
  <div id="info"></div>
</div>

<script>
  function addP() {
      var newP = document.createElement("p");
      var txtNode = document.createTextNode("이건 텍스트");
      newP.appendChild(txtNode);
      document.getElementById("info").appendChild(newP);
  }
</script>
```

<br>

# 속성값이 있는 새로운 요소 추가하기

1. 요소 노드 만들기 
   
   `createElement()`

2. 속성 노드 만들기
   
   `document.createAttribute(속성명)` 
   
   ex)
   
   ```javascript
   var srcNode = document.createAttribute("src");
   var altNode = document.createAttribute("alt");
   srcNode.value = "images/domo.jpg";
   altNode.value = "이미" 
   ```

3. 속성 노드 연결하기
   
   `요소명.setAttributeNode(속성노드)` 
   
   새로 만든 속성 노드를 요소 노드에 추가하는 메소드 만약 추가할 속성이 요소 노드에 이미 들어 있다면 기존 속성 노드를 새 속성 노드로 대체한다.

4. 자식 노드 연결하기
   
   `appendChild()`

<br>

# 노드 삭제하기

노드를 삭제할 때 부모 노드에서만 자식 노드를 삭제할 수 있다. 따라서 부모 노드를 찾는 프로퍼티가 필요하다.

1. parentNode 프로퍼티
   
   `노드.parentNode` : 현재 노드의 부모 노드에 접근해서 부모 노드의 요소 노드를 반환

2. removeChild( ) 메서드
   
   `부모노드.removeChild(자식노드)` : 자식 노드를 삭제하는 역할
