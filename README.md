# 6월 1일 학습내용 요약
## 사용할수 없는 코드
* let 키워드와 const 키워드 : 구 버전의 웹 브라우저에서느 let 키워드와 const 키워드를 사용할 수 없습니다 var 키워드를 사용해 변수를 만들어야 합니다

* 템플릿 문자열 : ECMAScirpt6에서 추가된 기능입니다. 문자열 연결 연산자를 사용합니다

* 화살표 함수 : 함수를 만들 때 반그시 function 키워드를 사용해야합니다

* for of 반복문 : for of 반목문 사용하고 싶을 때 for in 반복문을 사용해 대체해야합니다

* 사용할수 없는 메소드를 사용한 코드 : 배열과 관련된 처리를 할 때는 대부분 반복문을 사용해야 합니다.

## 브라우저 객체 모델
* 웹 브라우저와 관련된 객체를 브라우저 객체 모델이라고 합니다.
* document 객체는 큐모가 크므로 문서 객체 모델리이라고 따로 분류

## window 객체
* window 객체는 웹페이지 자체를 나타내고 사용하면 새로운 화면을 열거나 웹 브라우저의 크기를 변경하는 등의 일을 할 수 있습니다
* 경고창과 프롬프트

        alert() : 경고창을 출력합니다
        prompt() : 프롬프트를 출력합니다

## screen 객체
* 속성

        width : 화면의 너비
        height : 화면의 높이
        availWidth : 실제 화면에서 사용가능한 너비
        availHeight : 실제 화면에서 사용가능한 높이
        colorDepth : 사용가능한 색상 수
        pixelDepth : 한 픽셀당 비트 수

## location 객체와 history 객체
* 속성

        href : 문서의 URL 주소
        host : 호스트 이름과 포트 번호
        hostname : 호스트 이름
        port : 포트 번호
        pathname : 디렉터리 경로
        hash : 앵커 이름
        search : 요청 매개 변수
        protocol : 프로토콜 종류

* 메소드

        assing(링크) : 매개변수로 전당한 위ㅊ로 이동합니다
        reload() : 새로고침합니다 
        replace() : 매개 변수로 전달한 위치로 이동합니다

* history 메소드

        forward() : 앞으로 이동합니다
        back() : 뒤로 이동합니다

## navigator 객체
* 속성 

        appCodename : 웹브라우저의 코드 이름
        appName : 웹 브라우저의 코드 이름
        appVersion : 웹 브라우저의 버전
        platform : 사용 중인 운영체제의 시스템 환경
        userAgent : 웹 브라우저의 전체적인 정보

## 문서 객체 모델 관련 용어
* 웹 브라우저가 HTML 파일을 분석하고 출력하는 방식을 문서 객체 모델이라고 합니다.
* HTML 태그를 자바스크립트에서 사용할 수 있는 객체로 만든 것을 문서 객체라고 합니다.

## 웹 페이지 생성 순서
* 웹 브라우저가 웹 페이지를 실행하는 순서는 HTML 코드를 위에서 아래로 실행합니다.
* HTML 페이지의 생성 순서는 굉장히 중요합니다.

## 문서 객체 선택
* HTML 태그를 자바스크립트에서 문서 객체로 변환하는 것을 문서 객체 선택이라고 합니다
* 한 개의 객체를 선택하는 메소드

        document.getElementByld(아이디) : 아이디를 사용해 문서 객체를 선택합니다
        document.querySelector(선택자) : 선택자를 사용해 문서 객체를 선택합니다

* 여러 개의 객체를 선택하는 메소드

        document.getElementByName(이름) : name 속성으로 여러 개의 문서 객체를 선택합니다
        document.getElementByClassName(클래스) : class 속성으로 여러 개의 문서 객체를 선택합니다
        document.querySelectorAll(선택자) : 선택자를 사용해 여러 개의 문서 객체를 선택합니다

## 문서 객체 조작
* 문자 조작 : 문서 객체 내부의 문자를 조작할 때는 innerHTML 속성을 사용합니다

        innerHTML : 문서 객체 내부의 글자를 나타냅니다.

* 스타일 조작 : 문서 객체의 스타일을 조작할 때는 style 속성을 사용합니다. style 속성에는 CSS로 선택할 수 있는 모든 스타일 속성이 들어 있습니다.

        background-color : backgroundColor
        border=radius : borderRadius
        border=bottom : borderBottom

* 속성 조작

        setAttribute() : 속성을 지정합니다
        getAttribute() : 속성을 추출합니다

## 이벤트
* 키보드로 키를 입력하거나 마우스 클릭 등 어떤 현상이 프로그램에 영향을 미치는 것을 의미

        마우스 이벤트
        키보드 이벤트
        HTML 프레임 이벤트
        HTML 입력 양식 이벤트
        사용자 인터페이스 이벤트
        구조 변화 이벤트
        터치 이벤트

* 이벤트 관련 용어 정리 : 문서 객체에 이벤트를 연결하는 방법은 이벤트 모델이라고 한다. 

* 인라인 이벤트 모델 : 인라인 이벤트 모델은 HTML 태그 내부에서 이번트를 연결하는 방법입니다. 인라인 코드 내부에서 세미콜론을 사용해 문장을 구분하면 여러 줄의 코드를 입력할 수 있습니다

* 고전 이벤트 모델 : 이름은 고젠 이벤트 모델이지만 현대엗 많이 사용합니다. 인라인 이벤트 모델을 확실하게 이해했다면 고전 이벤트 모델도 쉽게 사용할 수 있습니다

* 이벤트 객체 : 자바스크립트도 마찬가지로 이벤트가 발생하면 이벤트 객체를 사용해 관련 정보를 알아낼 수 있습니다.

* 기본 이벤트 제거 : HTML 태그에는 기본 이벤트가 있습니다. 예를 들어 a 태그를 클릭하면 href 속성에 입력한 위치로 이동하고 form 태그 내부에서 <제출> 버튼을 누르면 자동으로 입력 양식을 제출합니다. 이게 기본 이벤트라고 합니다.

## jQuery 사용 준비
* jQuery 다운로드 페이지에서 jQuery 파일을 다운로드하거나 CDN 경로를 구할 수 있습니다

* jQuery를 사용하는 방법은 두가지가 있다. 첫번째는 특정 폴더에 파일을 다운로드한 후 HTML 페이지로 가져오는 것, 두번째는 CDN를 활용하는 것이다

## jQuery 객체
* jQuery 라이브러리는 $ 함수는 활용합니다. ex) $ 함수의 매개 변수에는 문서 객체.css 형식, HTML 형식의 문자열

## 문서 객체 선택
* 객체 탐색 메소드

        parent() : 부모 태그를 선택합니다.
        find() : 후손 태그를 찾습니다.

## 문서 객체 개별 조작
* 선택된 문서 객체의 수

        length : 선택된 문서 객체의 수를 구합니다

* 선택된 문서 객체 추출

        get() : 선택한 문서 객체 중 하나를 선택합니다

* 선택된 문서 객체 반복 적용

        each() : 선택한 문서 객체에 반복을 적용합니다

## 문서 객체 조작
* 문자 조작 

        text() : html 태그 내부의 문자를 조작
        html() : html 태그 내부의 문자를 조작 (html 태그 인식)

* text(), html() 메소드는 다음 방법으로 내부 문자를 가져올 수 있습니다
* 스타일 조작

        css() : 스타일을 조작합니다

* 스타일도 GET형태와 SET형태를 나누어 사용합니다

* 속성 조작

        attr() : 속성을 조작합니다

* 속성도 GET 형태와 SET형태로 나누어 사용합니다 GETㅎ형태는 선택자로 선택된 문저 객체중 첫 번쨰 문서 객체의 속성을 가져옵니다

## 문서 객체 생성
* 문서 객체를 생성할 때는 다음과 같이 $() 함수의 매개 변수에 HTML 형식의 문자열을 입력합니다

* 문서 객체 추가 메소드

        $(A).prependTO(B) : A를 B 안쪽 앞에 추가
        $(A).appendTO(B) : A를 B 안쪽 뒤에 추가
        $(A).insertBefore(B) : A를 B 앞에 추가
        $(A).insertAfter(B) : A를 B 뒤에 추가

## 이벤트
* 이벤트

        on() : 이벤트를 연결합니다
        off() : 이벤트를 제거합니다

* 이벤트 직접 연결 : 이벤트 직접 연결은 특정 태그에 이벤트를 연결하고 특정 태그를 눌렀을 때 이벤트가 발생하게 하는 것을 의미

* 키보드 이벤트

        keydown() : 키보드 키를 눌렀을 때
        keypress() : 키가 입력되었을 때
        keyup() : 키보드 키를 떼었을 때

* 마우스 이벤트

        click() : 마우스를 클릭했을 때
        dbclick() : 마우스 더블 클릭했을 떄
        mousedown() : 마우스 버튼을 눌렀을 때
        mouseenter() : 마우스 커서가 해당 태그로 들어갔을 때
        mouseleave() : 마우스 커서가 해당 태그로 나갔을 때
        mousemove() : 마우스가 움직일 때
        mouseup() : 마우스 버튼을 땔 떄

* 입력 양식 이벤트

        blur() : 입력 양식에 값 입력을 종료할 때
        change() : 입력 양식에 값 변경될 때
        focus() : 입력 양식에 값 입력을 시작할 때
        select() : type 속성이 select인 입력 양식의 목록에서 값을 선택했을 때
        submit() : type 속성이 submit인 입력 양식을 클릭했을 때

* 웹 브라우저 이벤트

        resize() : 웹 브라우저의 크기를 변경할 때
        scroll() : 웹 브라우저를 스크롤할 때

* 이벤트 직접 연결은 연결하는 시점에 존재하는 문서 객체에만 이벤트를 연결합니다. 이것은 문서 객체를 생성했을 때 이벤트를 따로 연결해서 해결할 수 있습니다.

* 이벤트 간접 연결 : 부모에게 이벤트를 위임해서 부모가 이벤트를 처리하게 하는 것이라고 할 수 있습니다

* 이벤트 제거 : 이벤트를 제거할 때는 off() 메소드를 사용합니다

        one() : 이벤트를 한번만 연결합니다

## 애니메이션 
* 기본적인 자바스크립트로도 할 수는 있지만 굉장히 어려운 작업이 있습니다.
* 애니메이션을 웹 브라우저가 제공하는 기본적인 API로만 구현하려면 굉장히 복잡해서 외부라이브러리를 사용합니다
* 애니메이션은 스타일에 적용하는데 숫자를 적용할 수 있는 모든 속성에 animate() 메소드를 사용

# 5월 25일 내용 요약
## 요청과 응답
* 웹 서버가 하는 일은 요청과 응답의 연속이라고 정의할 수 있습니다

* 웹 브라우저의 요청을 받은 웹 서버는 요청을 받아들여 웹페이지를 전송합니다. 웹페이지를 응답받은 웹 브라우저는 웹 페이지 화면을 띄웁니다

* 클라이언트가 서버에 HTML 페이지나 파일을 요청하면 서버가 그 요청에 응답해 요청한 HTML 페이지나 파일을 클라이언트에 제공하는 장소이다

## express 모듈을 사용한 서버 생성과 실행
* express 모듈 메소드

        express() : 서버 애플리케이션 객체를 생성합니다
        app.use() : 요청이 왔을 때 실행할 함수를 지정합니다
        app.listen() : 서버를 실행합니다

## 페이지 라우팅
* express 모듈은 app 객체의 다음 메소드를 활용해서 페이지 라우팅합니다
* 페이지 라우팅을 할 때는 토큰을 활용할 수 있습니다 토큰은 '<토큰 이름>' 형태로 설정합니다

## 요청과 응답 (2)
* response 객체

        send() : 데이터 본문을 제공합니다
        status() : 상태 코드를 제공합니다
        set() : 헤더를 설정합니다

* 데이터 제공 : send() 메소드를 가장 마지막에 실행해야 하며 두번 실행 할 수 없습니다

* Content-Type : 서버가 Content-Type을 제공해주면 웹 브라우저는 헤더를 확인하고, 제공된 데이터의 형태를 확인합니다 이때 형태는 MIME라는 문자열로 제공한다. MIME 형식은 굉장히 많기 떄문에 보통은 활용할 때 마다 찾아봅니다.

* HTTP 상태 코드

        1XX : 처리중
        2xx : 성공
        3xx : 리다이렉트
        4xx : 클라이언트 오류
        5xx : 서버 오류
        status() : 상태 코드를 지정합니다

* 리다이렉트 : 웹브라우저가 리다이렉트를 확인하면 화면을 출력하지 않고 응답 헤더에 있는 Location 속성을 확인해서 해당 위치로 이동

        redirect() : 리다이렉트합니다

* request 객체 (요청 매개 변수) : 요청 매개 변수를 추출할 때는 query 객체를 사용하고 URL 뒤에 ?기호를 삽입하고 '<키>=<값>' 형태로 값을 &로 구분해서 입력합니다

## 미들웨어
* express 모듈은 헤더, 상태코드 본문을 활용하여 코드를 조합하면 원하는 형태의 모든 서버를 만들어낼 수있는데 이를 쉽게 활용할 수있도록 여러 기능을 제공한다

* 정적파일제공 : 웹 페이지에서 변경되지 않은 요소를 쉽게 제공해주는 기능, 정적파일을 잘못 제공해서 실질적인 코드를 넘겨주는 실수를 할 수있으니 주의

* morgan 미들웨어 : 다른사람이 만든 미들웨어도 가져와서 사용가능, 로그 출력 미들웨어는 웹 요청과 관련된 내용을 출력하는 미들웨어이면 기본적이면서 중요한 미들웨어이다

* body-parser 미들웨어 : 요청 본문을 분석해줍니다

* 클라이언트에서 서버로 데이터 전송 : 클라이언트가 서버로 데이터 전송하는 방법은 굉장히 많습니다 ex) URL 입력, 요청애개변수 사용 , 응답 본문 사용

* 요청 본문 : 서버가 클라이언트로 데이터 전달할 때 응답 본문과 함께 전달, 클라이언트도 서버로 본문을 전달할 때 요청 본문의 종류를 함께 전달

* 속성 정리 

        params 객체 : URL의 토큰을 나타냅니다. 보기가 편합니다
        query 객체 : URL의 요청 매개 변수를 나타냅니다. 토큰보다 많은 데이터를 전달할 수 있으며 주소로 어떤 데이터가 오고 있는지 확인
        body 객체 : 대용량 문자열 등을 전송할때 사용, 다만 주소에 데이터를 기록하지 못하므로 새로고침이나 즐겨찾기 기능등을 활용할수 없습니다

## RESTful 웹 서비스 개요
* RESTful 웹 서비스는 REST 규정에 맞게 만든 ROA를 따르는 웹서비스 디자인 표준입니다

        GET : 컬렉션을 조회 / 컬렉션의 특정 요소를 조회
        POST : 컬렉션에 새로운 데이터를 추가 / 사용 x
        PUT : 컬렉션 전체에 한꺼번에 변경 / 컬렉션에 특정 요소 수정
        DELETE : 컬렉션 전체를 삭제 / 컬렉션 특정 요소 삭제


# 5월 18일 내용 요약
## 전역 변수
* 아무런 제약 없이 사용할 수 있는 변수

        __filename : 현재 실행 중인 코드의 파일 경로를 나타냅니다.
        __dirname : 현재 실행 중인 코드의 폴더 경로를 나타냅니다.

## prcess 객체의 속성과 이벤트
* 프로세스 정보를 제공하면 제어할수 있게하는 객체

        env : 컴퓨터 환경 정보를 나타냅니다
        version : Node.js 버전을 나타냅니다
        versions : Node.js와 종속된 프로그램 버전을 나타냅니다
        arch : 프로세서의 아키텍처를 나타냅니다
        platform : 플랫폼을 나타냅니다

* 메소드

        exit([exitCode = 0]) : 프로그램을 종료합니다
        memoryUsage() : 메모리 사용 정보 객체를 리턴합니다
        uptime() : 현재 프로그램이 실행된 시간을 리턴합니다

## process 객체와 이벤트 개요
* on(<이벤트 이름>, <이벤트 핸들러>) : 이벤트를 연결합니다
* 이벤트 핸들러(또는 이벤트 리스너)는 이벤트가 발생했을 떄 호출할 함수를 의미합니다

        exit : 프로세스가 종료될 때 발생합니다
        upcaughtException : 예외가 일어날 때 발생합니다

* 이벤트 핸들러의 매개 변수로 전달되는 매개변수를 '이벤트 매개 변수'라고 합니다

## os 모듈
* os 모듈은 애플리케이션을 만들 때 많이 활용하지 않는데 모듈의 기본 사용 방법을 익히기에 가장 적당합니다

## url 모듈
* 메소드

        parse() : URL 문자열을 URL 객체로 변환해 리턴합니다
        format() : URL 객체를 URL 문자열로 변환해 리턴합니다'
        resolve() : 매개변수를 조합하여 완전한 URL 문자열을 생성해 리턴합니다
        
## File System 모듈
* File System 모듈에는 파일 이름 수정, 이동, 제거 등 메소드가 정말 많습니다.

* 파일 읽기 메소드

        fs.readFileSync(<파일 이름>) : 동기적으로 파일을 읽어 들입니다.
        fs.readFile(<파일 이름>, <콜백함수>) : 비동기적으로 파일을 읽어 들입니다.

* 비동기 처리의 장점 : 자바스크립트 프로그래밍 언어는 C++, 자바보다 느립니다 하지만 프로그램을 개발하는 과정에서 Node.js를 사용하면 손쉽게 비동기처리를 구현할 수 있습니다
* 파일 쓰기 : 파일을 읽고 쓰는 방법을 알아봅시다

        fs.writeFileSync(<파일 이름>, <문자열>) : 동기적으로 파일을 씁니다
        fs.writeFile(<파일 이름>, <문자열>, <콜백 함수>) : 비동기적으로 파일을 씁니다

* 파일 처리와 예외처리 : 동기 코드를 예외처리 할 때는 try catch 구문을 활용하고, 비동기 코드를 예외 처리할 때는 콜백 함수로 전달된 첫 번째 매개 변수 error를 활용합니다

## 노드 패키지 매니저
* 어떤 프로그래밍 플랫폼이 기본적으로 제공하는 모듈을 '내부 모듈'이라고 합니다
* 내부 모듈을 조합해서 사용하기 쉬운 형태로 만들거나 새로운 기능을 구현해서 제공하는 것을 외부 모듈이라고 합니다

## request 모듈
* 웹 요청을 쉽게 만들어주는 모듈이고 다른 개인이 제공하는 외부 모듈입니다
* Github 페이지에 들어가면 해당 모듈과 관련된 자세한 설명이 있습니다

## cheerio 모듈
* request 모듈로 가져온 웹 페이지는 단순한 HTML 문자열이고 cheerio 모듈을 사용하면 가져온 웹페이지의 특정 위치에서 손쉽게 데이터를 추출할 수 있습니다
* request 모듈와 cheerio 모듈을 사용하면 자신이 원하는 다양한 정보를 손쉽게 가져올 수 있습니다

## asymc 모듈
* 대부분의 메소드가 비동기적으로 구성되므로 실행 순서 실행 순서를 정의하기가 어렵고, 들여쓰기도 많습니다. 이 문제를 어느정도 해결해 줄 수 있는 모듈이다

# 5월 11일 학습내용 요약
## Date 객체
* Date 객체 생성 방법

        new Date() : 현재 시간으로 Date 객체 생성
        new Date(유닉스 타임) : 유닉스 타임으로 Date 객체 생성
        new Date(시간 문자열) : 문자열로 Date 객체 생성
        new Date(년, 월-1, 일, 시간, 분, 초, 밀리초) : 시간 요소를 기반으로 Date 객체 생성 (0은 1월이므로 월에 -1를 해준다)

* <메소드>
        
         Date 객체는 get ㅇㅇ() 형태, set ㅇㅇ형태의 메소드를 가진다
        ㅇㅇ에 들어가는 문잔 Fullyear,Month,Day,Hours,Minutes.Seconds등이다

## array 객체
* 여러 자료를 다룰떄 사용하는 자료형입니다
* <메소드>

        concat() : 매개변수로 입력한 배열의 요소를 모두 합쳐 배열을 만들어 리턴
        join(): 배열 안의 모든 요소를 문자열로 만들어 리턴
        pop() : 배열의 마지막 요소를 제거하고 리턴
        push() : 배열의 마지막 부분에 새로운 요소를 추가
        reverse() : 배열의 요소 순서를 뒤집습니다
        slice() : 배열 요소의 지정한 부분을 지정한 부분을 리턴
        sort() : 배열의 요소를 정렬
        splice() : 배열 요소의 지정한 부분을 삭제하고 삭제한 요소를 리턴

## ECMAScript5에서 추가된 메소드
* Array 객체에 엄청나게 많은 메소드가 추가

        forEach() : 배열의 요소를 하나씩 뽑아 반복을 돌립니다
        map() : 콜백함수에서 리턴하는 것을 기반으로 새로운 배열 생성
        filter() : 콜백함수에서 true를 리턴하는 것으로만 새로운 배열을 만들어 리턴

## 조금 더 나아가기
* 프로토타입에 메소드를 추가하면 해당 자료형 전체에 추가할수 있습니다.
'
## JSON 객체
* JavaScript Object Notation의 약어로 자바스크립트 객체를 사용한 데이터 표현 방법입니다
* 몇가지 제약이 있다

        문자열은 큰따옴표로 만들어야 합니다
        모든 키는 큰따옴표로 감싸야 합니다
        숫자, 문자열, 불자료형만 사용할 수 있습니다

* <메소드>

        JSON.stringify(객체, 변환함수 공백개수)
        JSON.parse(문자열)

## 예외와 기본 예외 처리
* 프로그램을 실행하는 동안 문제가 발생하면 프로그램이 자동으로 중단되는데 그게 발생하는 오류를 예외라고 한다
* 그 오류에 대처하는게 예외 처리라고한다
* 자바스크립트에서는 오류와 예외를 구분하지않고 모두 '오류'로 칭합니다

## 고급 예외 처리
* 고급 예외처리는 try 키워드, catch 키워드, finally 키워드로 예외를 처리하는 방법입니다

        try {
                // 예외가 발생하면
        } catch (exception) {
                // 여기서 처리합니다
        } finally {
                // 여기는 무조건 실행합니다
        }
## 예외 객체
* catch 구문의 괄호 안에 들어 있는 변수를 나타냅니다
* 예외객체에는 name 속성과 message 속성이 있는데 이를 활용하여 자바스크립트로 웹서버를 만들때 개발자의 메일 등으로 오류 정보를 정리해서 보낼 수 있다

        try {

        } catch (excepttion) {

        }

## 예외 강제 발생
* 예외를 강제로 발생 시킬 때는 THROW 키워드로 사용 throw 키워드 뒤에는 문자열 또는 error 객체를 입력

        throw '강제 예외';

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
