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

  * window 객체에서 제공하는 대화형 함수

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

* __연산자(operator) `===`, `!==`__ 

```js
 const opTest =()=>{
            let check1 = 1;
            let check2 = "1";

            console.log(check1 == 1);    //true
            console.log(check1 == "1");  //true
            console.log(check2 == 1);    //true
            console.log(check2 == "1");  //true
            
            console.log('================');

            console.log(check1 === 1);   //true
            console.log(check1 !== "1"); //true
            console.log(check2 !== 1);   //true
            console.log(check2 === "1"); //true
        }
```

---

* __object__
  * 관련된 데이터와 함수의 집합.
  * 구성: 함수, 속성, this, 프로토타입
  * 키값을 사용하여 속성을 식별한다. 

```js
 //객체 작성1
        function myClass504(){
            this.name = "멀티캠퍼스";  //외부에서 접근 가능
            let name02 = "504강의실";  //외부에서 접근 불가능
            this.getName02 = function(){
                return name02;
            }
        }

 //객체 작성2 (많이씀)
        const myClass504_2 = {
            name: "멀티 캠퍼스",
            print:function(){
                alert(myClass504_2.name+ " : print");
            }
        }
        
        
 //프로토타입
        myClass504.prototype.printName=function(){
            let abc = "메롱";
            alert(this.name + ", " + this.getName02() + " : prototype " + abc);
        }


function objTest(){
    let cls = new myClass504();

    console.log(cls.name);
    console.log(cls.name02);
    console.log(cls.getName02());

    // let cls2 = new myClass504_2();
    // console.log(lcs2.name);  오류
    alert(myClass504_2.name);
    myClass504_2.print();

    // window.alert(); //객체안에 alert이라는 함수실행!!

    cls.printName(); 
}
```

---

* __Number__

```js
//1.작성방법
let num = new Number(7);
let num2 = 7;
console.log(num + ", " + num2);

//메소드
num = "12";
Number.parseInt(num);
```

---

* __transObject(형변환)__

  * 정수형 형변환 parseInt()

  ```js
   let vals = Number.parseInt(15);
  ```

  * 실수형 형변환 parseFloat()

  ```js
  let vals = parseFloat(15.33);
  ```

---

* __Math__

```js
<script>
        function test1(){
console.log("반올림: " + Math.round(123.456*100)/100);//반올림
console.log("내림: " + Math.floor(123.456*10)/10);//내림
console.log("올림: " + Math.ceil(123.456));//올림
}
</script>
```

---

* __string__
  * __대문자 변환__: `toUpperCase()`
  * __소문자 변환__: `toLowerCase()`
  * __글자 탐색__:`indexOf('탐색할 글자')`
  * __글자 잘라서 보기__: `substring(index위치,원하는index위치)`
  * __글자합치기__: `concat()`

