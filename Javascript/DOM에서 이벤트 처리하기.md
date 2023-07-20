# DOM 요소에 함수 직접 연결하기

```html
(...)
<img src="images/cup-1.png" id="cup">
(...)
<script>
    var cup = documnet.querySelector("#cup");
    cup.onclick = function(){
    alert("이미지를 클릭했습니다.);
}
</script>
```

이렇게 DOM 요소에 직접 이벤트 처리기를 연결할 수 있다.

위의 예시의 경우 cup에 id가 cup인 노드를 불러와 연결 후 그 노드가 클릭이벤트가 발생하면 함수를 출력하도록 연결해뒀다

<br>

# 함수 이름을 사용해 연결하기

```html
(...)
<img src="images/cup-1.png" id="cup">
(...)
<script>
    var cup = documnet.querySelector("#cup");
    cup.onclick = changepic;

    function changepic(){
          cup.src = "images/cup-2.png";
  }
}
</script>
```

<br>

# DOM의 event 객체 알아보기

DOM에는 이벤트 정보를 저장하는 event 객체가 있다.

```html
(...)
<img src="images/cup-1.png" id="cup">
(...)
<script>
    var cup = documnet.querySelector("#cup");
    cup.onclick = function(event) {
          alert("이벤트 유형: " + event.type + ", 이벤트 발생 위치: " + event.pageX + "," + event.pageY);
  }
}
</script>
```

1. event의 주요 프로퍼티
   
   ![](C:\Users\luili\Desktop\coding_study\Do_it_web\image\image_19.png)

2. 메서드
   
   ![](C:\Users\luili\Desktop\coding_study\Do_it_web\image\image_20.png)

<p></p>

event 객체에는 이벤트 정보만 들어 있다. 만약 이벤트가 발생한 대상에 접근하려면 이벤트 처리기에서 예약어 this를 사용해야 한다

```html
(...)
<img src="images/cup-1.png" id="cup">
(...)
<script>
    var cup = documnet.querySelector("#cup");
    cup.onclick = function(event) {
          alert("클릭한 이미지 파일: " + this.src);
  }
}
</script>
```

<br>

# CSS 속성에 접근하기

`document.요소명.style.속성명`

ex) id가 desc인 요소의 글자색 바꾸기

`document.getElementById("desc").style.color = "bule";`

하이픈이 있는 속성은 두 단어를 합쳐서 사용하되, 두 번째 단어의 첫 글짜는 대문자로 표시해야 한다.

ex) background-color 을 backgroundColor처럼 사용

<br>

```html
(...)
<div id="rect"></div>
(...)
<script>
    var myRect = document.querySelector("#rect");
    myRect.addEventListener("mouseover",function() {
        myRect.style.backgroundColor = "green";
        myRect.style.borderRadius = "50%";
        }
    );
```
