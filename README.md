# 5월 4일 학습내용 요약
## 생성자 함수
* 객체를 만드는 함수입니다

        function Product(name, prcie) {
                this.name = name;
                this.price = prcie;
        }

## 프로토타입
* 모든함수가 가지고 있는 속성으로 해당 함수를 생성자 함수로 사용했을때만 의미가 있습니다

        function Product(name, price) {
                this.name = name;
                this.price = prcie;
        }

        Product.prototype.print = function {
                console.log('$(product.name)의 가격은 $(product.price)원입니다.');
        }
        let product = new Product("바나나", 1200);
        product.print();

## 기본 자료형과 객체 자료형의 차이
* 숫자,문자열,블을 기본 자료형이라고 합니다

        let number = 273;
        let string = '안녕하세요';
        let boolean = true;

        console.log(type of number);
        console.log(type of string);
        console.log(type of boolean);
* 기본 자료형은 객체가 아니므로 속성과 메소드를 추가할 수 없습니다.

## Number 객체
* 자바스크립트에서 숫자를 표현할때 사용

        let numberFromLiteral = 273
        let numberFromConstructor = new Number(273);

* <메소드>
> toExponential() : 숫자를 지수 표시로 나타낸 문자열을 리턴합니다

> toFixed() : 숫자를 고정소수점 표시로 나타낸 문자열을 리턴합니다

> toPrecision() : 숫자를 길이에 따라 지수표시 또는 고정소수점 표시로 나타낸 문자열을 리턴합니다

* 생성자 함수의 속성
> MAX_VALUE : 자바스크립트의 숫자가 나타낼 수 있는 최대 숫자

> MIN_VALUE : 자바스크립트의 숫자가 나타낼 수 있는 최소 숫자

> Nan : 자바스크립트의 숫자로 나타낼 수 없는 숫자

> POSITIVE_INFINITY : 양의 무한대숫자

> NEGATIVE_INFINITY : 음의 무한대숫자

## String 객체
* 자바스크립트에서 가장 많이 사용하는 내장 객체

* <메소드>
> length : 문자열의 길이를 나타냅니다

* 자기 자신을 변화시키는 메소드를 파괴적 메소드라고 하고 자기 자신을 변화시키지 않은 리턴하는 메소드를 비파괴적 메소드라고 한다

# 4월 27일 수업 내용 요약
## 객체
* 여러개의 자료형을 한번에 저장하는 자료형
* 배열과 객체는 유사한 점이 있지만 다른점은 배열는 요소에 접근할떄 인덱스를 사용, 객체는 키를 사용

        let product = {
                제품명: '7D 건조 망고'
                유형: '당절임'
                성분: '망고, 설탕 메타중이황산나트륨, 치자황색소'
                원산지: '필라핀'
        };
        console.log(product);
        = { 제품명: '7D 건조 망고'
            유형: '당절임'
            성분: '망고, 설탕 메타중이황산나트륨, 치자황색소'
            원산지: '필라핀' }

## 객체와 반복문
* 생성한 객체에 for in 반복문으로 반복을 적용할 수 있다
* 일반적인 개발에서는 거의 사용하지 않는다

## 속성과 메소드
* 객체 내부에 있는 값 하나하나는 속성이라고 함
* 객체의 속성 중 자료형이 함수인 속성을 메소드라고 함

        let object = {
                name: '바나나'
                price: 1200
                print: function (){
                        console.log('($this.name)의 가격은 ($this.price)원입니다.')
                }
        }
        = 바나나의 가격은 1200원입니다

## 생성자 함수와 프로토타입
* 자바스크립트도 객체 지향 프로그래밍 언어의 일종이다
* 배열과 객체를 사용하면 여러개의 데이터를 쉽게 다룰 수 있습니다 

        let object = {
                name: '바나나'
                price: 1200
                print: function (){
                        console.log('($this.name)의 가격은 ($this.price)원입니다.')
                }
        }
이것을 간단하게 바꿀수있습니다.
         
         let object = {
                { name: '바나나', price: 1200 }
         };
         
# 4월 13일 학습내용
## 익명함수
* 기본형태 
> let <함수이름> = function () {};

        let root = function () {
                console.log("함수의 첫번쨰 줄");
                console.log("함수의 두번쨰 줄");
        };
        root ();
        console.log(root);
        => 함수의 첫번쨰 줄
           함수의 두번쨰 줄
* 함수 내부의 코드 덩어리를 만들고 console.log로 함수 내부의 코드 덩어리를 불러온다
* 이름이 없는 함수라서 이름이 출력 되지 않는다
## 선언적 함수
* 기본형태
> function <함수이름> {  }

        function root () {
                console.log("함수의 첫번쨰 줄");
                console.log("함수의 두번쨰 줄");
        };
        root ();
        console.log(root);
        => 함수의 첫번쨰 줄
           함수의 두번쨰 줄
           [Function: 함수]
* 익명함수와 달리 이름까지 출력되서 나온다
## 화살표 함수
* 기본형태
> () => { }

        let root = () => {
                console.log("함수의 첫번쨰 줄");
                console.log("함수의 두번쨰 줄");
        };
        root ();
        console.log(root);
        => 함수의 첫번쨰 줄
           함수의 두번쨰 줄
           [Function]
 * 대부분의 익명 함수 코드는 화살표 함수로 대체할수 있다

## 함수의 기본형태
* 기본형태

        function <함수이름> (<매개변수>) {
                <함수 코드>
                return <리턴 값>
        }        

* 매개 변수를 넣으면 메소드 내부에서 특정한 처리를 수행하고 값을 반환하는것

        function power(x) {
                return x * x
        }
        console.log(power(10));
        console.log(power(20));
        => 100
           400

* 함수는 매개변수를 여러개 가질수도 있습니다

        function power(x) {
                return x * y
        }
        console.log(power(10, 20));
        console.log(power(20, 30));
        => 200
           600

## 함수의 기본 활용 형태
* 기본형태

        function (<매개변수>, <매개변수>) {
                let output = <초깃값>;
                // output 계산
                return output;
        }        
* 예시

        function sum(min, max) {
                let output = 0;
                for (let i >= min; i <= max; i++) {
                        output += i;
                }
                return output;
        }
        console.log(sum(1, 100));
        => 5050

## 함수 매개 변수 초기화
* 매개변수를 입력하지 않아도 함수가 호출됩니다
* 매개 변수가 underfined인지 확읺하고 underfined일 때 문제가 발생한다면 따로 처리한다.
        
        function print(name, count) {
                console.log('$(name)이/가 $(count)개 있습니다.')
        }
        print ("사과", 10);
        print ("사과");
        => 사과이/가 10개 있습니다

## 콜백함수
* 함수를 변수에 저장할 수 있어 함수의 매개 변수로 전달할 수 있는 함수

        fuction callTenTimes(callback) {
                for (let i = 0; i < 5; i++) {
                        callback;
                }
        }
        callTenTimes(function()) {
                console.log('함수호출');
        });
        => 함수호출
           함수호출
           함수호출
           함수호출
           함수호출

## 표준 내장 함수
* 숫자 변환 함수 : 문자를 숫자로 변환하는 함수로 parseInt() 함수와 ParseInt () 함수를 제공
> parseInt() : 문자열을 정수로 변환합니다

> ParseInt () : 문자열을 실수로 변환합니다
# 4월 6일 학습내용 요약
## 역 for 반복문
* 배열 반복을 뒤에서부터 실행해야 할때가 있다. 이떄 사용한다

    let array = [1, 2, 3, 4, 5, 6];
    for (let i = array.length - 1; i >=0; i--) {
        console.log(array[i]);
    }
    => 6
    5
    4
    3
    2
    1

## for in 반복문과 for of 반복문
* 객체에 쉽게 반복문을 적용할 때 사용

    for ( let 인덱스 in 배열 ){
    
    }
    
    for ( let 요소 of 배열)  {

    }

    for (let i = 0; i < 배열,길이; i++)
    {
        
    let 인덱스 = i;

    let 요소 = 배열[ i ]
    
    }

## 중첩 반복문
* 반복문을 여러 번 중첩해서 사용하는 반복문

    let output = "";

    for (let i = 0; i < 10; i++) {
    
    for (let j = 1; j < i+1; j++) {
      
        output += "*";
    
    }
    
    output += "\n"

    }

    console.log(output);

=> 이 코드의 결과는 별 피라미드가 나오게 된다
## break 키워드
* 반복문도 항상 참이면 무한 반복인데 break 키워드를 사용하면 벗어날 수 있다 

    let i = 0;

    let array = [1, 31, 273, 57, 8, 11, 32]

    let output;

    while(true) {

    if (array[i] % 2 ==0) {

        output = array[i];

        break;

    }
    
    i = i + 1;

    }

    console.log ('발견한 짝수는 ${output}입니다')

    => 발견한 짝수는 8입니다

## continue 키워드
* 반복문 내부에서 현재 반복을 멈추고 다음 반복을 진행하게 한다

    for (let i = 1; i < 10; i++) {
    
    if (i % 2 == 0)
    
    {
        continue;
    
    }
    
    console.log(i);

}

=> 1 3 5 7 9

## 스코프
* 변수를 사용할 수 있는 범위를 나타낸다
* 자바스크립트에서는 블록 == 스코프라고 생각하면된다 

# [ 3월 16일 내용 요약 ]
## 자바스크립트의 발전
### 세계에서 가장 오해를 많이 받는 프로그래밍 언어
* 자바 스크립트은 부수적인 프로그래밍 언어로 취급
### 풍부한 경험을 제공하는 인터넷 애플리케이션(RIA)
* 자바스크립트로만 만든 웹 페이지가 데스크톱에서 사용하는 애플리케이션의 형태를 가졌으며 기존의 지도에 비해 강력한 지도 ds
* RIA는 Rich Internet Application의 약어로 풍부한 경험을 선사하는 웹 애플케이션을 의미합니다
### Node.js
* 크롬의 베타 버전 발표 이후 자바스크립트를 웹 브라우저가 아닌 곳에서도 사용할 수 있게 하자는 의견이 많아지면서 CommomJS 표준과 V8 자바스크립트 엔진을 기반으로 Node.js를 개발
* 스레드 : 효울적인 비동기 방식으로 프로그래밍 언어로 구현하는 방법
* Node.js 모든 모듈(라이브러리)이 비동기 기반의 프로그램을 만들 수 있도록 설계되어 초보자도 쉽게 프로그램을 만들 수 있음
## 자바스크립트로 할 수 있는 일
### 웹 클라이언트 애플리케이션 개발
* 자바스크립트는 웹 개발목적 으로 만들어졌다
* 웹 브라우저에서 실행할 수 있는 유일한 프로그래밍 언어
### 웹 서버 개발 (Node.js)
* 기존에는 웹개발은 두개 이상의 프로그래밍 언어가 필요(웹 클라이언트, 웹서버를 다른언어로 개발)
* Node.js가 등장하면서 자바스크립트로 웹서버 개발
* 웹 페이지를 출력하지 않아도 웹 프로토콜을 활용하여 웹서버로 칭하고 페이팔 결제 시스템에도 활용
* 웹 개발과 관련해서 간단한 모듈들만 제공해서 빠르긴 하지만 데이터, 예외 처리등이 복잡하다
### 모바일 애플리케이션 개발
< 네이티브 애플리케이션 >
* 스마트폰에서 인식할 수 있는 프로그래밍 언어로 만든 애플리케이션
* 2개의 애플리케이션 개발 시 시간, 인력 등이 비용도 2배가 들어간다
* 자바스크립트를 사용하여 1개의 애플리케이션만 개발해도 모든 스마트폰에서 동작가능
* 자바스크립트로 네이티브 애플리케이션을 개발할수 있는 React Native를 만들어 페이스북에서 공개
### 데스크톱 애플리케이션 개발
* 자바스크립트로 개발 전용 텍스트 에디터를 만들어 배포, 본격적으로 데스크톱 애플리케이션 개발
### 게임 개발
* 원래 게임은 서버와 클라이언트 모두 C++로 제작
* 한번에 여러 스마트폰 운영체제에서 실행할 수있는 애플리케이션을 개발 하는 것이 경제적으로 이득이 됨
* 자바스크립트를 기반으로 한 게임엔진인 유니티 등장
### 데이터베이스 관리
* 데이터를 저장할때 사용하는 프로그램
* 사용하기 쉬운 NoSQL 데이터베이스 등장
## 실습 환경 구축
### Atom 에디터 설치
* Atom 자바스크립트로 만든 텍스트 에디터
* Atom 에디터 사이트에서 다운받아 설치
### Node.js 설치
* Node.js 플랫폼은 다운로드 
> 홀수 버전 : 새로운 기능을 추가된 개발 버젼

> 짝수 버전 : 30개월 이상의 장기 지원하는 안정 버전
### 크롬설치
* 자바스크립트 코드를 실행할수있는 플랫폼으로 오류 확인이 쉬운 웹브라우저
## 기본 실습 방법
### 파일 생성
* Atom 에디터 [file] → [New file] → [file] → [save] → .js 확장자 이름을 붙혀 저장 → console.log("hello world..!")코드 입력
### 명령 프롬프트
* cmd를 입력하여 명령 프롬프트 실행
* node 명령어로 생성한 파일실행

< 명령 프롬프트 기본 명령어 >
> dir : 현재 폴더의 내용을 출력합니다

> cd <폴더이름> : <폴더이름>으로 이동합니다
* shift + 우클릭 여기서 명령창 열기
## 기본언어
* 표현식 : 간단한 코드 
* 문장 끝에 ;를 종결의 의미로 표현
* 키워드 : 특별한 의미가 부여된 단어
* 식별자 : 이름을 붙일 때 사용하는 단어
(함수의 이름,여러 단어로 된 식별자는 항상 대문자로 시작, 변수,속성 등의 이름은 소문자로 시작)
* 주석 : 프로그램의 진행에 영향을 주지 않은 코드
### 출력
* 출력 메소드 : console 의 log()메소드 사용하는 것으로 기본적인 출력 방법
* RELP를 사용한 출력 : 곧바로 문장을 입력하여 출력 확인
### 기본자료
* 숫자 : 가장 기본적인 자료형 
(예시 : console log(32); ,console log(3 + 2); )
* 문자열 : 문자의 집합
(예시 : console log("32"); ,console log("/나이/"); )


# 3월 23일
## 문자열
* 문자 선택 연산자 : 문자열 연결 연산자(+)로 문자열을 서로 연결합니다

        ex) console.log("가나다" + "라마");
        => 가나다라마
* 문자 선택 연산자 : 몇번째 있는 문자들을 선택합니다

        ex) console.log("안녕하세요"[0]);
        => 안

* 템플릿 문자열 : '기호로 생성하고 생성할 때 내부에 ${<표현식>}을 사용할 수 있고 계산되어 문자열에 들어갑니다 

        ex) '올해는 ' + new Date().getFullYear() + '년입니다'
        => '올해는 2021년입니다'

* 불 : 참과 거짓으로 표현할때 사용, true와 false 두가지 밖에 없다 (표 2-9 참고)
        ex) console.log( 52 < 273 );
        => true
* 비교 연산자 : 크기를 비교하는 연산자 (표 2-10 참고)


* 논리 부정 연산자 : 피연산자를 한개만 가지고 있는 단항 연산자이다
    > 논리합 연산자 : true가 한개라도 있으면 전체가 true가 되는 연산자이고 or라고 합니다

    > 논리곱 연산자 : false가 한개라도 있으면 전체가 false가 되는 연산자이고 and라고 합니다
## 변수
* 값을 저장할때 사용하는 식별자, 숫자뿐만 아니라 모든 자료형 저장가능 

    " let 식별자; "식으로 사용

        ex) let pi;
        => undefined
        pi = 3.14159265;
        => undefined
## 복합대입 연산자
* 자료형에 적용하는 기본 연산자와 =연산자를 함께 사용해 다음과 같이 구성합니다 (표 2-13, 표 2-14 참고)

        ex) let output = 0;
        output += 52;
        => 52
## 증감 연산자
* 변수 앞과 뒤에 ++, --기호를 붙여 만듭니다 (표 2-15 참고)

        ex) let number = 10;
        number++;
        => 11
## 자료형 검사
* 자료형을 확인할 때 typeof 연산자를 사용하는데 typeof는 키워드이면서 단항연산자이다
        
        ex) typeof;
        => 'number'

## underfined 자료형
* '초기화되지 않은것'을 표현하는 자료형

        ex) let a;
        => undefined

## 강제 자료형 변환
* 어떤 자료형을 특정자료형으로 강제 변환하고싶을 때는 사용 (표 2-17 참고)
## Number() 함수와 NaN
* 문자열이나 불을 숫자 변환할 때 Number() 함수 사용

        ex) console.log(Number("52"));
        => 52
* NaN은 'Not a Number'의 줄임말로 '숫자 자료형이지만 숫자가 아닌것'을 의미
    > NaN은 무조건적으로 다릅니다
  NaN인지 확인할 때는 isNaN()함수을 사용합니다 
## Boolean()함수
* 자바스크립트에서 Boolean()함수를 사용하면 5개의 요소는 false로 변환
    > O, NaN, "[빈 문자열]", null, undefined
        
        let nan = Number("안녕하세요");
        let undefinedariable;

        console.log(Boolean(null));
        => fasle
## 자동 자료형 변환
* 일부 자료형을 상황에 따라 자동으로 변환
* 숫자와 문자열에 '+'연산자를 적용하면 자동으로 숫자가 문자열로 변환

        ex) console.log("52 + 273");
        => 52273
* 조건문의 조건 표현식을 넣을 떄와 ! 연산자를 사용할 때는 불자료형으로 전환

        ex) let nan = Number("안녕하세요");
        let undefinedariable;

        console.log(!!0);
        => fasle
## 일치 연산자
* 비교 연산자와 달리 자료형까지 일치해야 'true'라는 결과가 나온다

        === : 자료형과 값이 같은지 비교합니다
        !== : 자료형과 값이 다른지 비교합니다

## 상수 
* 상수 : '항상 같은 수'라는 의미로 변수와 반대되는 개념, '변경하지 않을 대상'에 상수를 적용
* 상수를 사용하고 오류가 발생하면 변수(let)로 교체합니다
## if 조건문
* if (<불 표현식>) {}형식으로 사용합니다, 불 표현식이 true이면 문장을 실행하고
fasle이면 문장을 무시합니다

        let input = 32;
        if (input % 2 == 0) {
        console.log("짝수입니다");}
        => 짝수입니다
## if else 조건문
*  if (<불 표현식>) {}형식으로 사용합니다, 불 표현식이 거짓일때 실행한다

        let input = 33;
        if (input % 2 == 0) {
        console.log("짝수입니다");
        } else {
                console.log("홀수입니다");
        }
        => 홀수입니다
# 3월 30일 내용 요약
## 중첩 조건문
* 조건문 안에 조건문을 사용하는 것

        let date = new Date();
        let hours = date.getHours();
        if (hours < 11>) {
                console.log("아침 먹을 시간입니다");
        } else if (hours < 15>) {
                console.log("점심 먹을 시간입니다");
        else {
                console.log("저녁 먹을 시간입니다");

        => 점심 먹을 시간입니다

## if else if 조건문
* 조건이 한문장이라면 조건문의 중괄호를 생략가능, 중복되지 않은 세가지이상의 조건을 구분항 때 사용
* 중첩 조건문 예제 참조

## switch 조건문
* swich 조건문 기본 형태

        switch (<비교할 값>) {
                case <값>;
                <문장>
                break;
                case <값>;
                <문장>
                break;
        default:
                <문장>
                break;
        }

* break 키워드는 switch 조건문을 빠져 나갈 때 사용
* 입력한 표현식과 case 키워드 옆에 있는 표현식이 같다면 case 키워드 다음에 오는 문장을 차례대로 실행
* 범위를 표현해야한다면 IF조건문을 사용
## 삼항 연산자
* 프로그램의 진행을 조건에 따라 변화 시킬 수 있는 연산자
* 기본 형태 : <불 표현식> ? <참> : <거짓>

        let numberA 52;

        console.log('${numberA}은/는 ${numberA > 0 ? "0보다 큰" : "0 또는 0보다 작은"} 숫자입니다.');

        => 52은/는 0보다 큰 숫자입니다

## 짧은 초기화 조건문
* 삼항 연산자를 사용해 변수가 underfined일때만 초기화합니다
>  A || B 에서 A가 참이라면 A로 대치됩니다

> A || B 에서 A가 거짓이면 B로 대치됩니다

        let test;
        test = test || "초기화합니다_1"
        console.log(test);
        test = test || "초기화합니다_2"
        console.log(test);

        => 초기화합니다_1
           초기화합니다_1

## 배열
* 여러개의 자료를 한꺼번에 다룰수 있는 자료형
* 형태 : let 이름 = [자료, 자료, 자료]

        > let array = [52, 273, true, '아침밤']
        > console.log(array[2]);
        => 273

## while 반복문
* 가장 기본적인 반복문, 표현식이 참인 동안에는 중괄호안의 문장을 계속 실행

        while (<불 표현식>) {
                계속 실행시킬 문장
        }
* 조건이 항상 참일 경우에는 무한 반복문이 된다

## for 반복문
* for 반복문은 원하는 횟수만큼 반복이 가능
* 순서를 이렇게 진행된다

        1. 초기식을 비교한다
        2. 조건식을 비교한다. 조건이 false이면 반복문 종료
        3. 문장을 실행
        4. 종결식을 실행
        5. 2단계로 이동

* 기본형태

        for (let = i 0; i< <반복 횟수>; i++) {

        }
* 예시

        let output = 0
        for (let i =0; i <= 100; i++){
                output + = i;
        }
        console.log(output);
