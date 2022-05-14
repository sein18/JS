# JS

* __변수 선언__

  * var (호스팅)
  * let
  * const

  ```js
  <script type="text/javascript">
          console.log(test1);//밑에 var변수 처리해주니 undifine정의(에러 안뜸) var는 호이스팅
          var test1=1; 
          console.log(test1);
  
          // console.log(test2);
          let test2= 2;
          console.log(test2);
  
          const test3 = 3; //불변
          console.log(test3);
          
          {
              var no=10;
              let no2=20;
              const no3=30;
              
              console.log(no);
              console.log(no2);
              console.log(no3);
          }
          console.log(no);
          // console.log(no2);
          // console.log(no3);
          
          console.log('========');
          
          num=10;
          console.log(num);
  </script>
  ```

---

* __변수의 사용__
  * 선언 규칙
    1. 대소문자 구분.(NO no)
    2. 영문, $, _로 시작해야 한다.
    3. 영문, $, _, 숫자를 포함할 수 있다.
    4. 키워드나 예약어를 사용할 수 없다.



---

* __자바스크립트 작성방식 3가지__(CSS방식과 유사)
  * `inline`  방식
  * 내부작성 방식(embedded)
  * 외부 작성 방식



---

* __범위__

  * 전역변수

  ```js
   let variable=10;
  function test01(){
              variable = variable + 5;
              document.getElementById("v01").innerHTML = "<b style='color:red; background:yellow;'>"+variable+"</b>";
  }
  ```

  * 지역변수

  ```js
    function test02(){
              const variable2 = variable + 100;
              document.getElementById("v02").innerHTML = "<b>"+variable2+"</b>";
    }
  ```

---

