# Age-Calculator

<img src="./Age Calculator.gif">

## 기능

태어난 날짜를 입력 후 버튼을 클릭하면, 사용자가 입력한 값을 받아서 오늘 날짜 기준으로 나이를 계산    
<br>
## 학습
### 1. js : new Date()    
: 자바스크립트의 날짜 객체는 new Date()를 이용하여 생성  
: 메서드 및 속성   
|속성|의미|
|---|---|
|.getFullYear|Date에서 현지 시간 기준 연도(네 자리 연도면 네 자리로)를 반환합니다.|
|.getMonth()|Date에서 현지 시간 기준 월(0–11)을 반환합니다.|
|.getDate()|Date에서 현지 시간 기준 일(1–31)을 반환합니다.|
<br>     

### 2. js: innerHTML vs  vs textContent 의 차이  
**(1) innerHTML**  
: 'Element'의 속성으로, element내에 포함 된 HTML 또는 XML 마크업을 가져오거나 태그와 함께 입력하여 내용을 직접 설정할 수 있음  
: 즉, innerHTML을 사용하면 내부 HTML 코드를 JavaScript 코드에서 새 내용으로 쉽게 변경할 수 있음  
 ```
<!-- innerHtml예시 -->

const innerH = document.getElementById('innerH');
innerH.innerHTML = "<div style='color:red'>innerHTML</div>";
console.log(innerH)
// 스타일 적용된 빨간색 폰트로 innerHTML 출력
```

**(2) innerText**    
: 'Element'의 속성으로, element내에서 사용자에게 보여지는 text값들을 가져오거나 설정할 수 있다.  

```
<!-- innerText예시 -->

const innerT = document.getElementById('innerT');
innerT.innerText = "<div style='color:red'>innerText</div>";
console.log(innerT)

// 스타일 적용되지 않은 기본 폰트로 <div style='color:red'>innerText</div> 출력
```
**(3) textContent**  
: 'Node'의 속성으로, 사용자에게 보여지는 text값만 읽어오는 innetText와는 달리 \<script\>나 \<style\> 태그에 상관없이 해당 노드가 가지고 있는 텍스트 값을 모두 읽어온다.
```
<div id="box">
    <style>#source {color: blue}</style>
    <p>Hi there!</p>
    <span style="display: none">hidden message</span>
</div>

<!-- innerText의 경우 -->
console.log(box.innerText);
// Hi there!
// 눈에 보이는 텍스트만 반환  

<!-- textContent의 경우 -->
 console.log(box.textContent);
 // #source {color: blue}
    Hi there!
    hidden message
// 눈에 보이지 않는 모든 요소의 텍스트 컨텐츠까지 가져옴  
```

<br> 

## 학습출처  
- https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Date#%EC%83%9D%EC%84%B1%EC%9E%90
- https://www.w3schools.com/jsref/jsref_obj_date.asp
- https://veggie-garden.tistory.com/5  
- https://velog.io/@kim_unknown_/JavaScript-Difftext 
