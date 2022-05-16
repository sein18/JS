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

* __function함수__

  *  window 객체에서 제공하는 대화형 함수

    * __console.log()__

    ```js
     function prnConsole(){
                window.console.log('콘솔에 출력하기'); //console.log('콘솔에 출력하기');
            }
    ```

    * __alert__

    ```js
     function alertTest(){
                window.alert('내용 출력'); //alert('내용 출력');
            }
    ```

    * __confirm__

    ```js
    function confirmTest(){
        // let test = window.confirm('2교시가 맞나요?'); //confirm('2교시가 맞나요?');
        // console.log(test);
    
          if(confirm('배경을 분홍색으로 바꿀까요?')){
              document.body.style.backgroundColor = "pink"; 
          }else{
              console.log("기본 색상 유지");
              document.body.style.backgroundColor = "white";
          }
    }
    ```

    * __prompt__

    ```js
     function promptTest(){
            //    let test = window.prompt("입력하세요."); //prompt("입력하세요.");
            //    console.log(test); //취소시 null이 뜬다.
            
                const txt = prompt("좋아하는 과목 번호를 선택해 주세요. \n[1.java 2.db 3.ui]"); //리턴 타입이 string이다
                switch(txt){ //Number(txt) 형변환 해줄 수 있다.
                    case "1":
                        console.log("역시 자바!!");
                        break;
                    case "2":
                        console.log("와우 디비~");
                        break;
                    case "3":
                        console.log("오~ UI");
                        break;
                    default:
                    console.log("1,2,3 중에 하나만 선택해주세요.");
                }
            }
    ```

---

* __DOM(Document Object Model) 탐색 함수__

  * __document.getElementById__

  ```js
  let doc = document.getElementById("id명");
  id가 들어간 태그의 정보를 가져온다.
  ```

  * __document.getElementsByName__

  ```js
  let doc = document.getElementsByName("name명");
  name으로 들어간 태그들을 전부 배열로 가져온다.
  ```

  * __document.getElementsByTagName__

  ```js
  let doc = document.getElementsByTagName("태그");
  태그에 들어있는 모든 정보를 배열로 가져온다.
  ```



---

