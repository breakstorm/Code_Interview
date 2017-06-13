**Table of Contents**

- [체크리스트](#%EC%B2%B4%ED%81%AC%EB%A6%AC%EC%8A%A4%ED%8A%B8)
    - [자바스크립트 scope를 var키워드를 기준으로 설명할수 있다.](#%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-scope%EB%A5%BC-var%ED%82%A4%EC%9B%8C%EB%93%9C%EB%A5%BC-%EA%B8%B0%EC%A4%80%EC%9C%BC%EB%A1%9C-%EC%84%A4%EB%AA%85%ED%95%A0%EC%88%98-%EC%9E%88%EB%8B%A4)
        - [[예제 1] 함수 단위의 유효 범위](#%EC%98%88%EC%A0%9C-1-%ED%95%A8%EC%88%98-%EB%8B%A8%EC%9C%84%EC%9D%98-%EC%9C%A0%ED%9A%A8-%EB%B2%94%EC%9C%84)
        - [[예제 2] 변수명의 중복 허용](#%EC%98%88%EC%A0%9C-2-%EB%B3%80%EC%88%98%EB%AA%85%EC%9D%98-%EC%A4%91%EB%B3%B5-%ED%97%88%EC%9A%A9)
        - [[예제 3] var 키워드의 생략](#%EC%98%88%EC%A0%9C-3-var-%ED%82%A4%EC%9B%8C%EB%93%9C%EC%9D%98-%EC%83%9D%EB%9E%B5)
        - [[예제 4] 렉시컬 특성](#%EC%98%88%EC%A0%9C-4-%EB%A0%89%EC%8B%9C%EC%BB%AC-%ED%8A%B9%EC%84%B1)
    - [closure 는 언제 형성되는지? 경험한 코드가 있으면 코드로 보여주기.](#closure-%EB%8A%94-%EC%96%B8%EC%A0%9C-%ED%98%95%EC%84%B1%EB%90%98%EB%8A%94%EC%A7%80-%EA%B2%BD%ED%97%98%ED%95%9C-%EC%BD%94%EB%93%9C%EA%B0%80-%EC%9E%88%EC%9C%BC%EB%A9%B4-%EC%BD%94%EB%93%9C%EB%A1%9C-%EB%B3%B4%EC%97%AC%EC%A3%BC%EA%B8%B0)
        - [[예제 1] 내부 변수 참조 값 접근](#%EC%98%88%EC%A0%9C-1-%EB%82%B4%EB%B6%80-%EB%B3%80%EC%88%98-%EC%B0%B8%EC%A1%B0-%EA%B0%92-%EC%A0%91%EA%B7%BC)
        - [[예제 2] 다른 객체로 내부 변수 참조](#%EC%98%88%EC%A0%9C-2-%EB%8B%A4%EB%A5%B8-%EA%B0%9D%EC%B2%B4%EB%A1%9C-%EB%82%B4%EB%B6%80-%EB%B3%80%EC%88%98-%EC%B0%B8%EC%A1%B0)
        - [클로저의 사용이유](#%ED%81%B4%EB%A1%9C%EC%A0%80%EC%9D%98-%EC%82%AC%EC%9A%A9%EC%9D%B4%EC%9C%A0)
    - [const는 언제 사용해야 하는지?](#const%EB%8A%94-%EC%96%B8%EC%A0%9C-%EC%82%AC%EC%9A%A9%ED%95%B4%EC%95%BC-%ED%95%98%EB%8A%94%EC%A7%80)
        - [let](#let)
        - [const](#const)
    - [mvc방식으로 개발한 사례가 있다면 본인이 느끼는 장단점을 설명하기.](#mvc%EB%B0%A9%EC%8B%9D%EC%9C%BC%EB%A1%9C-%EA%B0%9C%EB%B0%9C%ED%95%9C-%EC%82%AC%EB%A1%80%EA%B0%80-%EC%9E%88%EB%8B%A4%EB%A9%B4-%EB%B3%B8%EC%9D%B8%EC%9D%B4-%EB%8A%90%EB%81%BC%EB%8A%94-%EC%9E%A5%EB%8B%A8%EC%A0%90%EC%9D%84-%EC%84%A4%EB%AA%85%ED%95%98%EA%B8%B0)
    - [크롬개발자도구에서 js디버깅을 하는 방식을 설명해보기.](#%ED%81%AC%EB%A1%AC%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%8F%84%EA%B5%AC%EC%97%90%EC%84%9C-js%EB%94%94%EB%B2%84%EA%B9%85%EC%9D%84-%ED%95%98%EB%8A%94-%EB%B0%A9%EC%8B%9D%EC%9D%84-%EC%84%A4%EB%AA%85%ED%95%B4%EB%B3%B4%EA%B8%B0)
    - [비동기 콜백함수와 스택간의 관계를 어떻게 설명할 수 있는지?](#%EB%B9%84%EB%8F%99%EA%B8%B0-%EC%BD%9C%EB%B0%B1%ED%95%A8%EC%88%98%EC%99%80-%EC%8A%A4%ED%83%9D%EA%B0%84%EC%9D%98-%EA%B4%80%EA%B3%84%EB%A5%BC-%EC%96%B4%EB%96%BB%EA%B2%8C-%EC%84%A4%EB%AA%85%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8A%94%EC%A7%80)
    - [DOM 조작과정에서 성능에 좋지 않은 방식과 좋은 사례는 어떤 것들이 있는지?](#dom-%EC%A1%B0%EC%9E%91%EA%B3%BC%EC%A0%95%EC%97%90%EC%84%9C-%EC%84%B1%EB%8A%A5%EC%97%90-%EC%A2%8B%EC%A7%80-%EC%95%8A%EC%9D%80-%EB%B0%A9%EC%8B%9D%EA%B3%BC-%EC%A2%8B%EC%9D%80-%EC%82%AC%EB%A1%80%EB%8A%94-%EC%96%B4%EB%96%A4-%EA%B2%83%EB%93%A4%EC%9D%B4-%EC%9E%88%EB%8A%94%EC%A7%80)
        - [좋지 않은 예](#%EC%A2%8B%EC%A7%80-%EC%95%8A%EC%9D%80-%EC%98%88)
        - [좋은 예](#%EC%A2%8B%EC%9D%80-%EC%98%88)
    - [배열에서 제공하는 메서드 중에 filter와 map의 활용경험은?](#%EB%B0%B0%EC%97%B4%EC%97%90%EC%84%9C-%EC%A0%9C%EA%B3%B5%ED%95%98%EB%8A%94-%EB%A9%94%EC%84%9C%EB%93%9C-%EC%A4%91%EC%97%90-filter%EC%99%80-map%EC%9D%98-%ED%99%9C%EC%9A%A9%EA%B2%BD%ED%97%98%EC%9D%80)
    - [prototype 이 가진 장점은 무엇인가?](#prototype-%EC%9D%B4-%EA%B0%80%EC%A7%84-%EC%9E%A5%EC%A0%90%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [prototype 을 통해 객체를 만드는 방법에 대해서 설명하기.](#prototype-%EC%9D%84-%ED%86%B5%ED%95%B4-%EA%B0%9D%EC%B2%B4%EB%A5%BC-%EB%A7%8C%EB%93%9C%EB%8A%94-%EB%B0%A9%EB%B2%95%EC%97%90-%EB%8C%80%ED%95%B4%EC%84%9C-%EC%84%A4%EB%AA%85%ED%95%98%EA%B8%B0)
    - [es6에서 본인이 생각할때 지난번대비 개선된 점은 무엇이고, 왜 그렇게 생각하는지?](#es6%EC%97%90%EC%84%9C-%EB%B3%B8%EC%9D%B8%EC%9D%B4-%EC%83%9D%EA%B0%81%ED%95%A0%EB%95%8C-%EC%A7%80%EB%82%9C%EB%B2%88%EB%8C%80%EB%B9%84-%EA%B0%9C%EC%84%A0%EB%90%9C-%EC%A0%90%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B4%EA%B3%A0-%EC%99%9C-%EA%B7%B8%EB%A0%87%EA%B2%8C-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94%EC%A7%80)
    - [event delegation의 원리는 무엇인지? 적용한 경험이 있다면 어떤기능이였는지?](#event-delegation%EC%9D%98-%EC%9B%90%EB%A6%AC%EB%8A%94-%EB%AC%B4%EC%97%87%EC%9D%B8%EC%A7%80-%EC%A0%81%EC%9A%A9%ED%95%9C-%EA%B2%BD%ED%97%98%EC%9D%B4-%EC%9E%88%EB%8B%A4%EB%A9%B4-%EC%96%B4%EB%96%A4%EA%B8%B0%EB%8A%A5%EC%9D%B4%EC%98%80%EB%8A%94%EC%A7%80)
    - [좋은 코드를 만들기 위해서 노력한 경험들은 무엇인지?](#%EC%A2%8B%EC%9D%80-%EC%BD%94%EB%93%9C%EB%A5%BC-%EB%A7%8C%EB%93%A4%EA%B8%B0-%EC%9C%84%ED%95%B4%EC%84%9C-%EB%85%B8%EB%A0%A5%ED%95%9C-%EA%B2%BD%ED%97%98%EB%93%A4%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EC%A7%80)
    - [전역변수를 없앨 수 있는 방법들은 무엇인가?](#%EC%A0%84%EC%97%AD%EB%B3%80%EC%88%98%EB%A5%BC-%EC%97%86%EC%95%A8-%EC%88%98-%EC%9E%88%EB%8A%94-%EB%B0%A9%EB%B2%95%EB%93%A4%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [이벤트를 거쳐 API를 통해 dom조작까지 이어지는 과정을 순서대로 설명해보라.](#%EC%9D%B4%EB%B2%A4%ED%8A%B8%EB%A5%BC-%EA%B1%B0%EC%B3%90-api%EB%A5%BC-%ED%86%B5%ED%95%B4-dom%EC%A1%B0%EC%9E%91%EA%B9%8C%EC%A7%80-%EC%9D%B4%EC%96%B4%EC%A7%80%EB%8A%94-%EA%B3%BC%EC%A0%95%EC%9D%84-%EC%88%9C%EC%84%9C%EB%8C%80%EB%A1%9C-%EC%84%A4%EB%AA%85%ED%95%B4%EB%B3%B4%EB%9D%BC)
    - [setTimeout을 이용해 재귀호출을 하는 경우 어떤 장점이 있는가?](#settimeout%EC%9D%84-%EC%9D%B4%EC%9A%A9%ED%95%B4-%EC%9E%AC%EA%B7%80%ED%98%B8%EC%B6%9C%EC%9D%84-%ED%95%98%EB%8A%94-%EA%B2%BD%EC%9A%B0-%EC%96%B4%EB%96%A4-%EC%9E%A5%EC%A0%90%EC%9D%B4-%EC%9E%88%EB%8A%94%EA%B0%80)
    - [문제가 있을때 본인이 가장 자주 사용하는 디버깅 과정은 무엇인가?](#%EB%AC%B8%EC%A0%9C%EA%B0%80-%EC%9E%88%EC%9D%84%EB%95%8C-%EB%B3%B8%EC%9D%B8%EC%9D%B4-%EA%B0%80%EC%9E%A5-%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EB%94%94%EB%B2%84%EA%B9%85-%EA%B3%BC%EC%A0%95%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [github을 통해서 협업과정을 거치는 과정을 branch를 중심으로 설명하기.](#github%EC%9D%84-%ED%86%B5%ED%95%B4%EC%84%9C-%ED%98%91%EC%97%85%EA%B3%BC%EC%A0%95%EC%9D%84-%EA%B1%B0%EC%B9%98%EB%8A%94-%EA%B3%BC%EC%A0%95%EC%9D%84-branch%EB%A5%BC-%EC%A4%91%EC%8B%AC%EC%9C%BC%EB%A1%9C-%EC%84%A4%EB%AA%85%ED%95%98%EA%B8%B0)
    - [jQuery를 사용하는 것의 장점과 단점은 무엇이라고 생각하는지.](#jquery%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EA%B2%83%EC%9D%98-%EC%9E%A5%EC%A0%90%EA%B3%BC-%EB%8B%A8%EC%A0%90%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B4%EB%9D%BC%EA%B3%A0-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94%EC%A7%80)
    - [정규표현식으로 email을 체크해보기.](#%EC%A0%95%EA%B7%9C%ED%91%9C%ED%98%84%EC%8B%9D%EC%9C%BC%EB%A1%9C-email%EC%9D%84-%EC%B2%B4%ED%81%AC%ED%95%B4%EB%B3%B4%EA%B8%B0)
    - [요즘 관심있게 지켜보는 라이브러리나 오픈소스가 있다면 무엇인지? 어떤점이 마음에 드는지?](#%EC%9A%94%EC%A6%98-%EA%B4%80%EC%8B%AC%EC%9E%88%EA%B2%8C-%EC%A7%80%EC%BC%9C%EB%B3%B4%EB%8A%94-%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC%EB%82%98-%EC%98%A4%ED%94%88%EC%86%8C%EC%8A%A4%EA%B0%80-%EC%9E%88%EB%8B%A4%EB%A9%B4-%EB%AC%B4%EC%97%87%EC%9D%B8%EC%A7%80-%EC%96%B4%EB%96%A4%EC%A0%90%EC%9D%B4-%EB%A7%88%EC%9D%8C%EC%97%90-%EB%93%9C%EB%8A%94%EC%A7%80)
    - [서비스 성능개선을 했던 사례를 말해보자.](#%EC%84%9C%EB%B9%84%EC%8A%A4-%EC%84%B1%EB%8A%A5%EA%B0%9C%EC%84%A0%EC%9D%84-%ED%96%88%EB%8D%98-%EC%82%AC%EB%A1%80%EB%A5%BC-%EB%A7%90%ED%95%B4%EB%B3%B4%EC%9E%90)
    - [this 에 대해서 설명하기.](#this-%EC%97%90-%EB%8C%80%ED%95%B4%EC%84%9C-%EC%84%A4%EB%AA%85%ED%95%98%EA%B8%B0)
    - [this를 변경시킬 수 있는 방법을 코드로 예시로 보여주기.](#this%EB%A5%BC-%EB%B3%80%EA%B2%BD%EC%8B%9C%ED%82%AC-%EC%88%98-%EC%9E%88%EB%8A%94-%EB%B0%A9%EB%B2%95%EC%9D%84-%EC%BD%94%EB%93%9C%EB%A1%9C-%EC%98%88%EC%8B%9C%EB%A1%9C-%EB%B3%B4%EC%97%AC%EC%A3%BC%EA%B8%B0)
        - [[예제 1]](#%EC%98%88%EC%A0%9C-1)
        - [[예제 2]](#%EC%98%88%EC%A0%9C-2)
    - [bind 메서드의 내부 코드는 어떻게 됐을까?](#bind-%EB%A9%94%EC%84%9C%EB%93%9C%EC%9D%98-%EB%82%B4%EB%B6%80-%EC%BD%94%EB%93%9C%EB%8A%94-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%90%90%EC%9D%84%EA%B9%8C)
    - [IE9 지원이 필요하지만, ie9 에서 제공하지 않는 최신 javascript API를 사용하고 싶을때, 어떻게 대처할 것인가?](#ie9-%EC%A7%80%EC%9B%90%EC%9D%B4-%ED%95%84%EC%9A%94%ED%95%98%EC%A7%80%EB%A7%8C-ie9-%EC%97%90%EC%84%9C-%EC%A0%9C%EA%B3%B5%ED%95%98%EC%A7%80-%EC%95%8A%EB%8A%94-%EC%B5%9C%EC%8B%A0-javascript-api%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B3%A0-%EC%8B%B6%EC%9D%84%EB%95%8C-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%8C%80%EC%B2%98%ED%95%A0-%EA%B2%83%EC%9D%B8%EA%B0%80)
    - [팀장님이 내가 전혀 모르는 기능에 대한 개발을 부탁하면 어떻게 대응할 것인가?](#%ED%8C%80%EC%9E%A5%EB%8B%98%EC%9D%B4-%EB%82%B4%EA%B0%80-%EC%A0%84%ED%98%80-%EB%AA%A8%EB%A5%B4%EB%8A%94-%EA%B8%B0%EB%8A%A5%EC%97%90-%EB%8C%80%ED%95%9C-%EA%B0%9C%EB%B0%9C%EC%9D%84-%EB%B6%80%ED%83%81%ED%95%98%EB%A9%B4-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%8C%80%EC%9D%91%ED%95%A0-%EA%B2%83%EC%9D%B8%EA%B0%80)
    - [모듈패턴은 어떻게 구현할수 있는지? 모듈패턴의 어떤 장점이 있는지?](#%EB%AA%A8%EB%93%88%ED%8C%A8%ED%84%B4%EC%9D%80-%EC%96%B4%EB%96%BB%EA%B2%8C-%EA%B5%AC%ED%98%84%ED%95%A0%EC%88%98-%EC%9E%88%EB%8A%94%EC%A7%80-%EB%AA%A8%EB%93%88%ED%8C%A8%ED%84%B4%EC%9D%98-%EC%96%B4%EB%96%A4-%EC%9E%A5%EC%A0%90%EC%9D%B4-%EC%9E%88%EB%8A%94%EC%A7%80)
    - [javascript 코드를 html하단에 주로 배치하는 이유는 ?](#javascript-%EC%BD%94%EB%93%9C%EB%A5%BC-html%ED%95%98%EB%8B%A8%EC%97%90-%EC%A3%BC%EB%A1%9C-%EB%B0%B0%EC%B9%98%ED%95%98%EB%8A%94-%EC%9D%B4%EC%9C%A0%EB%8A%94-)
    - [javascript 코드를 여러개 html에 추가하는 것과, 하나로 머지하여 배포하는 것의 장단점은 무엇인가?](#javascript-%EC%BD%94%EB%93%9C%EB%A5%BC-%EC%97%AC%EB%9F%AC%EA%B0%9C-html%EC%97%90-%EC%B6%94%EA%B0%80%ED%95%98%EB%8A%94-%EA%B2%83%EA%B3%BC-%ED%95%98%EB%82%98%EB%A1%9C-%EB%A8%B8%EC%A7%80%ED%95%98%EC%97%AC-%EB%B0%B0%ED%8F%AC%ED%95%98%EB%8A%94-%EA%B2%83%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [html을 내려받으면서 브라우저가 화면에 모든것을 표현하기까지의 전체 렌더링 과정을 설명해보자.](#html%EC%9D%84-%EB%82%B4%EB%A0%A4%EB%B0%9B%EC%9C%BC%EB%A9%B4%EC%84%9C-%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80%EA%B0%80-%ED%99%94%EB%A9%B4%EC%97%90-%EB%AA%A8%EB%93%A0%EA%B2%83%EC%9D%84-%ED%91%9C%ED%98%84%ED%95%98%EA%B8%B0%EA%B9%8C%EC%A7%80%EC%9D%98-%EC%A0%84%EC%B2%B4-%EB%A0%8C%EB%8D%94%EB%A7%81-%EA%B3%BC%EC%A0%95%EC%9D%84-%EC%84%A4%EB%AA%85%ED%95%B4%EB%B3%B4%EC%9E%90)
    - [ecmascript란 무엇인가?](#ecmascript%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [코드리뷰를 했던 사례를 말해보라. 어떤점을 느꼈는가?](#%EC%BD%94%EB%93%9C%EB%A6%AC%EB%B7%B0%EB%A5%BC-%ED%96%88%EB%8D%98-%EC%82%AC%EB%A1%80%EB%A5%BC-%EB%A7%90%ED%95%B4%EB%B3%B4%EB%9D%BC-%EC%96%B4%EB%96%A4%EC%A0%90%EC%9D%84-%EB%8A%90%EA%BC%88%EB%8A%94%EA%B0%80)
    - [DOM Tree란 무엇인가?](#dom-tree%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [innerHTML을 직접 구현하면 어떻게 구현해야 할까?](#innerhtml%EC%9D%84-%EC%A7%81%EC%A0%91-%EA%B5%AC%ED%98%84%ED%95%98%EB%A9%B4-%EC%96%B4%EB%96%BB%EA%B2%8C-%EA%B5%AC%ED%98%84%ED%95%B4%EC%95%BC-%ED%95%A0%EA%B9%8C)
    - [유니크한 데이터를 집합으로 가지는 set을 array 로 구현하면 어떻게 구현할 수 있을까?](#%EC%9C%A0%EB%8B%88%ED%81%AC%ED%95%9C-%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%A5%BC-%EC%A7%91%ED%95%A9%EC%9C%BC%EB%A1%9C-%EA%B0%80%EC%A7%80%EB%8A%94-set%EC%9D%84-array-%EB%A1%9C-%EA%B5%AC%ED%98%84%ED%95%98%EB%A9%B4-%EC%96%B4%EB%96%BB%EA%B2%8C-%EA%B5%AC%ED%98%84%ED%95%A0-%EC%88%98-%EC%9E%88%EC%9D%84%EA%B9%8C)
    - [touch 이벤트와 mouse이벤트의 차이점은 무엇인가?](#touch-%EC%9D%B4%EB%B2%A4%ED%8A%B8%EC%99%80-mouse%EC%9D%B4%EB%B2%A4%ED%8A%B8%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
    - [preventDefault는 언제 쓸 수 있는 것인지?](#preventdefault%EB%8A%94-%EC%96%B8%EC%A0%9C-%EC%93%B8-%EC%88%98-%EC%9E%88%EB%8A%94-%EA%B2%83%EC%9D%B8%EC%A7%80)
    - [버블링과 캡처링을 설명하세요.](#%EB%B2%84%EB%B8%94%EB%A7%81%EA%B3%BC-%EC%BA%A1%EC%B2%98%EB%A7%81%EC%9D%84-%EC%84%A4%EB%AA%85%ED%95%98%EC%84%B8%EC%9A%94)
    - [배포나 릴리즈 전에 코드를 어떻게 테스트 할 수 있는지? 좋은 사례나, 경험을 말해보기.](#%EB%B0%B0%ED%8F%AC%EB%82%98-%EB%A6%B4%EB%A6%AC%EC%A6%88-%EC%A0%84%EC%97%90-%EC%BD%94%EB%93%9C%EB%A5%BC-%EC%96%B4%EB%96%BB%EA%B2%8C-%ED%85%8C%EC%8A%A4%ED%8A%B8-%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8A%94%EC%A7%80-%EC%A2%8B%EC%9D%80-%EC%82%AC%EB%A1%80%EB%82%98-%EA%B2%BD%ED%97%98%EC%9D%84-%EB%A7%90%ED%95%B4%EB%B3%B4%EA%B8%B0)
    - [콜백함수란 무엇인지 설명하기.](#%EC%BD%9C%EB%B0%B1%ED%95%A8%EC%88%98%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EC%A7%80-%EC%84%A4%EB%AA%85%ED%95%98%EA%B8%B0)
    - [template 을 어떻게 관리하는 게 좋다고 생각하는지 ?](#template-%EC%9D%84-%EC%96%B4%EB%96%BB%EA%B2%8C-%EA%B4%80%EB%A6%AC%ED%95%98%EB%8A%94-%EA%B2%8C-%EC%A2%8B%EB%8B%A4%EA%B3%A0-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94%EC%A7%80-)
    - [자바스크립트에서 빌드는 어떤 것을 하는 것일까? 사용해본 도구가 있는지?](#%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EC%97%90%EC%84%9C-%EB%B9%8C%EB%93%9C%EB%8A%94-%EC%96%B4%EB%96%A4-%EA%B2%83%EC%9D%84-%ED%95%98%EB%8A%94-%EA%B2%83%EC%9D%BC%EA%B9%8C-%EC%82%AC%EC%9A%A9%ED%95%B4%EB%B3%B8-%EB%8F%84%EA%B5%AC%EA%B0%80-%EC%9E%88%EB%8A%94%EC%A7%80)
    - [팀프로젝트에서 제일 중요한 부분은 무엇이라고 생각하는가?](#%ED%8C%80%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%97%90%EC%84%9C-%EC%A0%9C%EC%9D%BC-%EC%A4%91%EC%9A%94%ED%95%9C-%EB%B6%80%EB%B6%84%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B4%EB%9D%BC%EA%B3%A0-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94%EA%B0%80)
    - [커뮤니케이션을 잘하기 위해서 어떤 방법을 해보았는가?](#%EC%BB%A4%EB%AE%A4%EB%8B%88%EC%BC%80%EC%9D%B4%EC%85%98%EC%9D%84-%EC%9E%98%ED%95%98%EA%B8%B0-%EC%9C%84%ED%95%B4%EC%84%9C-%EC%96%B4%EB%96%A4-%EB%B0%A9%EB%B2%95%EC%9D%84-%ED%95%B4%EB%B3%B4%EC%95%98%EB%8A%94%EA%B0%80)
    - [커밋로그가 가진 의미는 어떤것일까? 어떤 규칙이 좋다고 생각하는지?](#%EC%BB%A4%EB%B0%8B%EB%A1%9C%EA%B7%B8%EA%B0%80-%EA%B0%80%EC%A7%84-%EC%9D%98%EB%AF%B8%EB%8A%94-%EC%96%B4%EB%96%A4%EA%B2%83%EC%9D%BC%EA%B9%8C-%EC%96%B4%EB%96%A4-%EA%B7%9C%EC%B9%99%EC%9D%B4-%EC%A2%8B%EB%8B%A4%EA%B3%A0-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94%EC%A7%80)
    - [less , sass를 써보았는가? 그것이 가진 장점은 무엇인지? 왜 그런것이 나왔다고 생각하는지?](#less--sass%EB%A5%BC-%EC%8D%A8%EB%B3%B4%EC%95%98%EB%8A%94%EA%B0%80-%EA%B7%B8%EA%B2%83%EC%9D%B4-%EA%B0%80%EC%A7%84-%EC%9E%A5%EC%A0%90%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EC%A7%80-%EC%99%9C-%EA%B7%B8%EB%9F%B0%EA%B2%83%EC%9D%B4-%EB%82%98%EC%99%94%EB%8B%A4%EA%B3%A0-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94%EC%A7%80)
    - [feature detection에 대해서 설명하시요.](#feature-detection%EC%97%90-%EB%8C%80%ED%95%B4%EC%84%9C-%EC%84%A4%EB%AA%85%ED%95%98%EC%8B%9C%EC%9A%94)
    - [모바일웹의 애니메이션 구현에 대한 경험과 가장 좋은 방식을 말해보세요.](#%EB%AA%A8%EB%B0%94%EC%9D%BC%EC%9B%B9%EC%9D%98-%EC%95%A0%EB%8B%88%EB%A9%94%EC%9D%B4%EC%85%98-%EA%B5%AC%ED%98%84%EC%97%90-%EB%8C%80%ED%95%9C-%EA%B2%BD%ED%97%98%EA%B3%BC-%EA%B0%80%EC%9E%A5-%EC%A2%8B%EC%9D%80-%EB%B0%A9%EC%8B%9D%EC%9D%84-%EB%A7%90%ED%95%B4%EB%B3%B4%EC%84%B8%EC%9A%94)
    - [웹화면에 가운데 정렬이 되는 모달다이얼로그를 어떻게 구현할 수 있을까?](#%EC%9B%B9%ED%99%94%EB%A9%B4%EC%97%90-%EA%B0%80%EC%9A%B4%EB%8D%B0-%EC%A0%95%EB%A0%AC%EC%9D%B4-%EB%90%98%EB%8A%94-%EB%AA%A8%EB%8B%AC%EB%8B%A4%EC%9D%B4%EC%96%BC%EB%A1%9C%EA%B7%B8%EB%A5%BC-%EC%96%B4%EB%96%BB%EA%B2%8C-%EA%B5%AC%ED%98%84%ED%95%A0-%EC%88%98-%EC%9E%88%EC%9D%84%EA%B9%8C)
    - [검색자동완성을 위한 수도코드를 작성해보세요.](#%EA%B2%80%EC%83%89%EC%9E%90%EB%8F%99%EC%99%84%EC%84%B1%EC%9D%84-%EC%9C%84%ED%95%9C-%EC%88%98%EB%8F%84%EC%BD%94%EB%93%9C%EB%A5%BC-%EC%9E%91%EC%84%B1%ED%95%B4%EB%B3%B4%EC%84%B8%EC%9A%94)
    - [merge 과정에서 생기는 충돌을 해결하는 과정을 설명하세요.](#merge-%EA%B3%BC%EC%A0%95%EC%97%90%EC%84%9C-%EC%83%9D%EA%B8%B0%EB%8A%94-%EC%B6%A9%EB%8F%8C%EC%9D%84-%ED%95%B4%EA%B2%B0%ED%95%98%EB%8A%94-%EA%B3%BC%EC%A0%95%EC%9D%84-%EC%84%A4%EB%AA%85%ED%95%98%EC%84%B8%EC%9A%94)
    - [REST API는 무엇인가?](#rest-api%EB%8A%94-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)
        - [리소스](#%EB%A6%AC%EC%86%8C%EC%8A%A4)
        - [메서드](#%EB%A9%94%EC%84%9C%EB%93%9C)
    - [post와 get의 차이점을 설명하세요.](#post%EC%99%80-get%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90%EC%9D%84-%EC%84%A4%EB%AA%85%ED%95%98%EC%84%B8%EC%9A%94)
    - [http header는 무엇인가요?](#http-header%EB%8A%94-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%EC%9A%94)
    - [javascript의 call stack에 대해서 설명하세요.](#javascript%EC%9D%98-call-stack%EC%97%90-%EB%8C%80%ED%95%B4%EC%84%9C-%EC%84%A4%EB%AA%85%ED%95%98%EC%84%B8%EC%9A%94)
    - [비동기 함수안에 비동기 로직이 또 있을때 이를 어떻게 보기 좋게 해결할 수 있을지 사례와 원리를 설명하세요.](#%EB%B9%84%EB%8F%99%EA%B8%B0-%ED%95%A8%EC%88%98%EC%95%88%EC%97%90-%EB%B9%84%EB%8F%99%EA%B8%B0-%EB%A1%9C%EC%A7%81%EC%9D%B4-%EB%98%90-%EC%9E%88%EC%9D%84%EB%95%8C-%EC%9D%B4%EB%A5%BC-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%B3%B4%EA%B8%B0-%EC%A2%8B%EA%B2%8C-%ED%95%B4%EA%B2%B0%ED%95%A0-%EC%88%98-%EC%9E%88%EC%9D%84%EC%A7%80-%EC%82%AC%EB%A1%80%EC%99%80-%EC%9B%90%EB%A6%AC%EB%A5%BC-%EC%84%A4%EB%AA%85%ED%95%98%EC%84%B8%EC%9A%94)
        - [[promise 선언부]](#promise-%EC%84%A0%EC%96%B8%EB%B6%80)
        - [[promise 실행부]](#promise-%EC%8B%A4%ED%96%89%EB%B6%80)
        - [[promise 에러처리]](#promise-%EC%97%90%EB%9F%AC%EC%B2%98%EB%A6%AC)
    - [네임스페이스 패턴의 장점은?](#%EB%84%A4%EC%9E%84%EC%8A%A4%ED%8E%98%EC%9D%B4%EC%8A%A4-%ED%8C%A8%ED%84%B4%EC%9D%98-%EC%9E%A5%EC%A0%90%EC%9D%80)
    - [react, vue, angular라이브러리 중 하나를 골라야할때 어떤식으로 고를 예정인가요?](#react-vue-angular%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC-%EC%A4%91-%ED%95%98%EB%82%98%EB%A5%BC-%EA%B3%A8%EB%9D%BC%EC%95%BC%ED%95%A0%EB%95%8C-%EC%96%B4%EB%96%A4%EC%8B%9D%EC%9C%BC%EB%A1%9C-%EA%B3%A0%EB%A5%BC-%EC%98%88%EC%A0%95%EC%9D%B8%EA%B0%80%EC%9A%94)
    - [개발시 어려움이 많거나 풀리지 않을경우 어떤 해결방법을 사용하는가?](#%EA%B0%9C%EB%B0%9C%EC%8B%9C-%EC%96%B4%EB%A0%A4%EC%9B%80%EC%9D%B4-%EB%A7%8E%EA%B1%B0%EB%82%98-%ED%92%80%EB%A6%AC%EC%A7%80-%EC%95%8A%EC%9D%84%EA%B2%BD%EC%9A%B0-%EC%96%B4%EB%96%A4-%ED%95%B4%EA%B2%B0%EB%B0%A9%EB%B2%95%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94%EA%B0%80)
    - [배워나가는 기술을 공유하거나 기록하는 것들이 있는지?](#%EB%B0%B0%EC%9B%8C%EB%82%98%EA%B0%80%EB%8A%94-%EA%B8%B0%EC%88%A0%EC%9D%84-%EA%B3%B5%EC%9C%A0%ED%95%98%EA%B1%B0%EB%82%98-%EA%B8%B0%EB%A1%9D%ED%95%98%EB%8A%94-%EA%B2%83%EB%93%A4%EC%9D%B4-%EC%9E%88%EB%8A%94%EC%A7%80)
    - [본인이 생각하는 가장 적절한 커밋단위는 ?](#%EB%B3%B8%EC%9D%B8%EC%9D%B4-%EC%83%9D%EA%B0%81%ED%95%98%EB%8A%94-%EA%B0%80%EC%9E%A5-%EC%A0%81%EC%A0%88%ED%95%9C-%EC%BB%A4%EB%B0%8B%EB%8B%A8%EC%9C%84%EB%8A%94-)
    - [디자이너와 기획자가 구현이 불가능할 것으로 예상되는 기능개발을 요구할때 대처방법은?](#%EB%94%94%EC%9E%90%EC%9D%B4%EB%84%88%EC%99%80-%EA%B8%B0%ED%9A%8D%EC%9E%90%EA%B0%80-%EA%B5%AC%ED%98%84%EC%9D%B4-%EB%B6%88%EA%B0%80%EB%8A%A5%ED%95%A0-%EA%B2%83%EC%9C%BC%EB%A1%9C-%EC%98%88%EC%83%81%EB%90%98%EB%8A%94-%EA%B8%B0%EB%8A%A5%EA%B0%9C%EB%B0%9C%EC%9D%84-%EC%9A%94%EA%B5%AC%ED%95%A0%EB%95%8C-%EB%8C%80%EC%B2%98%EB%B0%A9%EB%B2%95%EC%9D%80)
    - [front-end 개발자의 역할은 어디까지 일까?](#front-end-%EA%B0%9C%EB%B0%9C%EC%9E%90%EC%9D%98-%EC%97%AD%ED%95%A0%EC%9D%80-%EC%96%B4%EB%94%94%EA%B9%8C%EC%A7%80-%EC%9D%BC%EA%B9%8C)
    - [nodeJS의 설치방법과 모듈화를 통한 웹서버 라우팅을 구현할 수 있다.](#nodejs%EC%9D%98-%EC%84%A4%EC%B9%98%EB%B0%A9%EB%B2%95%EA%B3%BC-%EB%AA%A8%EB%93%88%ED%99%94%EB%A5%BC-%ED%86%B5%ED%95%9C-%EC%9B%B9%EC%84%9C%EB%B2%84-%EB%9D%BC%EC%9A%B0%ED%8C%85%EC%9D%84-%EA%B5%AC%ED%98%84%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8B%A4)

- [참조목록](#참조목록)  



## 체크리스트

### 자바스크립트 scope를 var키워드를 기준으로 설명할수 있다.
다른 언어와 다르게 자바스크립트는 유효 범위의 개념이 다르다
타 언어는 블록 단위로 스코프이지만 자바스크립트는 함수 단위로 스코프를 유지한다.

이러한 맥락에서 자바스크립트의 스코프 특징은 다음과 같다.
- 함수 단위의 유효 범위
- 변수명의 중복 허용
- var 키워드의 생략
- 렉시컬 특성 

##### [예제 1] 함수 단위의 유효 범위
```
function scopeTest() {  
    var a = 0;
    if (true) {
        var b = 0;
        for (var c = 0; c < 5; c++) {
            console.log("c=" + c);
         }
         console.log("c=" + c);
    }
    console.log("b=" + b);
}
scopeTest();  

//실행결과
c = 0  
c = 1  
c = 2  
c = 3  
c = 4  
c = 5  
b = 0  
```

다른 언어는 블록단위 이므로 if나 for 안에서만 scope가 형성되지만
자바스크립트는 함수 단위이므로 function을 기준으로 유효범위로 설정된다.

##### [예제 2] 변수명의 중복 허용
```
var scope = 10;  
function scopeExam(){  
    var scope = 20;
    console.log("scope = " +scope);
}
scopeExam();  

//실행결과
scope =20  
```

다른 언어와 달리 자바스크립트는 변수명이 중복되어도 에러가 발생하지 않는다.
단, 같은 범위에서의 변수명이 같다면 가까운 변수를 참조한다.
예를 들면, 위의 코드에서 같은 변수명이 호출되었을 때, 전역변수가 아닌 같은 함수 내에 있는 지역 변수 scope를 참조한다.

##### [예제 3] var 키워드의 생략
```
function scopeExam(){  
    scope = 20;
    console.log("scope = " +scope);
}

function scopeExam2(){  
    console.log("scope = " + scope);
}
scopeExam();  
scopeExam2();  

//실행결과
scope=20  
scope=20  
```

다른 언어에서 변수 타입을 생략하면 오류가 발생하지만, 자바스크립트는 var 키워드를 생략하고 변수선언이 가능하다. 그러나 이와 같은 경우에는 전역 변수로 선언이 된다. 따라서 위의 코드를 보면 function 안에서 선언했음에도 불구하고 외부 변수 scopeExam2에서 호출이 가능함을 볼수 있다.


##### [예제 4] 렉시컬 특성

```
function f1(){  
    var a= 10;
    f2();
}
function f2(){  
    return a;
}
f1();

//실행결과
Uncaught Reference Error  
: a is not defined
```

렉시컬 특성이란 함수 실행 시 유효 범위를 함수 실행 환경이 아닌 함수 정의 환경으로 참조하는 특성이다. 위의 코드를 보면 f1에 지역변수 a가 선언되어있고 내부에서 f2를 호출하는데, f2를 '선언할 때'  지역변수 a를 가져올수 없으므로 a의 값은 찾을수 없게 된다.

---

### closure 는 언제 형성되는지? 경험한 코드가 있으면 코드로 보여주기.
클로저는 자바스크립트의 scope chain을 이용하여 이미 생명주기가 끝난 외부 함수의 변수를 참조하는 방법을 말한다. 외부함수가 종료되더라도 내부함수가 실행되는 상태면 내부함수에서 참조하는 외부함수는 닫히지 못하고 내부함수에 의해서 닫히게 되어 클로저라고 불리게 된다.  

내부변수는 외부함수가 실행될 때마다 새로운 유효범위 체인과 새로운 내부 변수를 생성한다. 또, 클로저가 참조하는 내부 변수는 실제 내부 변수의 복사본이 아닌 그 내부변수를 직접 참조한다.

##### [예제 1] 내부 변수 참조 값 접근
```
// 외부 함수
function outerFunc(){
    // 내부 변수
    var a= 0;
    return {
        // 내부 함수(클로저)
        innerFunc1 : function(){
            a+=1;
            console.log("a :"+a);
        },
        // 내부 함수(클로저)
        innerFunc2 : function(){
            a+=2;
            console.log("a :"+a);
        }
    };
}
var out = outerFunc();  
out.innerFunc1();  
out.innerFunc2();  
out.innerFunc2();  
out.innerFunc1();

//실행결과
a = 1  
a = 3  
a = 5  
a = 6
```
클로저가 내부 변수에 접근하게 될 경우 값을 가져오는 것(call by value)이 아니라 참조(call by reference)하게된다. 따라서 innerFunc1과 innerFunc2는 참조에 의해 a에 접근하므로 a의 값이 계속 증가한다.


##### [예제 2] 다른 객체로 내부 변수 참조
```
function outerFunc(){  
    var a= 0;
    return {
        innerFunc1 : function(){
            a+=1;
            console.log("a :"+a);
        },
        innerFunc2 : function(){
            a+=2;
            console.log("a :"+a);
        }
    };
}
var out = outerFunc();  
var out2 = outerFunc();  
out.innerFunc1();  
out.innerFunc2();  
out2.innerFunc1();  
out2.innerFunc2();  

//실행결과
a = 1  
a = 3  
a = 1  
a = 3  
```
예제 1과 비슷해 보이지만 out과 out2라는 다른 객체로 내부 변수를 참조하게 된다. 객체가 생성될때마다 메모리에 서로 다른 내부변수가 생성되기 때문이다.


##### 클로저의 사용이유

클로저를 사용하게 되면 전역변수의 오/남용이 없는 깔끔한 코드를 사용할 수 있다. 때문에 클로저는 자바스크립트에서 적합한 방식의 패턴을 구현할 수있다. 이를 패턴화 한것이 모듈 패턴이다. 또한 자바스크립트에서 명시적으로 제공되지 않는 public/private, 즉, 공개 속성/함수, 비공개 속성/함수에 대한 구현이 가능하다.

---
### const는 언제 사용해야 하는지?
javascript es6로 넘어오면서 var의 뚜렷한 문제점인 전역 스코프로 인한 충돌의 해결책이 나오게 되었다. 기존의 var는 상당히 너그러워서, 변수가 중복선언되거나 사용되는 곳 아래에 선언되더라도(호이스팅) 크게 오류가 일어나지 않았다. 또한 var는 함수 단위의 스코프를 가지기 때문에 충돌이 많이 발생하게 되었다.

##### let
이를 해결하기위해 es6부터 let과 const 타입이 나오게 되었다. let은 블록 단위의 변수 타입이며 var보다 엄격하므로, 같은 스코프내에서 중복이나 호이스팅을 허용하지 않는다. 따라서 let의 유효범위는 {}, 브라켓 내부가 된다.

##### const
const는 타 언어에서 상수로 사용되는 변수 타입이다. 실제로 원시형 변수에 대해서는 const를 사용하게 되면 상수의 역할을 하게된다(초기값을 설정하지 않으면 에러 발생). 하지만 참조형 변수(Object, array, function)의 경우 const로 선언하는것이 좋은데, 참조형 변수의 경우 const로 선언하더라도 멤버값을 조작하는것이 가능하다. 이유는 해당 참조형 변수를 가르키는 값이 변한것이 아니라 메모리 내부의 변수값을 변경한 것이기 때문이다. 따라서 const로 지정된 참조형 변수의 참조값을 변경하려고 할 경우만 오류가 일어난다. 마찬가지로 블록 스코프를 가진다.

---
### mvc방식으로 개발한 사례가 있다면 본인이 느끼는 장단점을 설명하기.

```
```
---
### 크롬개발자도구에서 js디버깅을 하는 방식을 설명해보기.

```
```

---
### 비동기 콜백함수와 스택간의 관계를 어떻게 설명할 수 있는지?
비동기 콜백함수는 싱글 스레드 환경인 자바 스크립트에서 효율적인 코딩을 가능하게 한다. 자바스크립트는 싱글 스레드 환경이므로 하나의 콜스택을 가지게 되는데, 먼저 메인 컨텍스트가 호출되고 메인 함수 내부 함수들이 스택에 쌓이고 빠져나가면서 실행되어진다. 이때 콜백 함수를 호출하는 함수는 콜 스택에 쌓였다가 콜백함수를 web API에 등록하게 되며, 이 때 시간이 지나거나 response 요청을 받는등의 특정한 조건 후에 task queue(event queue)로 들어가게 된다. 모든 함수가 실행되고 콜스택이 비어있을때 task queue에 가장 첫번째 쌓인 콜백 함수부터 스택에 쌓이고 실행되며 task queue가 빌때까지 반복된다.

---
### DOM 조작과정에서 성능에 좋지 않은 방식과 좋은 사례는 어떤 것들이 있는지?
DOM은 javascritp core와 다르게 별도의 언어로 보아야한다. 따라서 독립적 API라고 볼수있는데, 이 때문에 DOM 객체에 접근을 위해서는 상당히 비싼 사용료를 내야한다. 따라서 루프문 안에서 DOM API를 조작하는 것은 나쁘며, 더 좋지 않은 것이 그 API를 이용하여 HTML 컬렉션을 조작하는 것이다. 따라서 DOM API 조작을 미루고 필요할 때 한번 DOM에 접근하는 것이 좋다.

- 리플로우 - DOM의 기하학적 위치를 새로 계산
- 리페인팅 - 리플로우 등으로 영향을 받은 부위를 새로 그림

리플로우와 리페인팅이 잦아질수록 느려지므로 랜더트리의 변경사항을 모아두었다가 한번에 처리하는 것이 유리하다.


##### 좋지 않은 예
```
var console = document.getElementById("console");
var lis = document.getElementsByTagName("il");
var len = lis.length;
for(var i = 0; i < len; i++) {
    console.innerHTML += li[i].innerHTML + "<br />";
}
```

##### 좋은 예

```
var console = document.getElementById("console");
var lis = document.getElementsByTagName("il");
var len = lis.length;
var cache = [];
for(var i = 0; i < len; i++) 
    // 일반적으로 이러한 문자열 결합은 +로 더해가는 것보다,
    // 배열을 사용하여 전부 요소로 등록하고 join을 쓰는 것이 빠르다.
    cache.push(li[i].innerHTML);
}
console.innerHTML = cache.join("<br />");
```

---
### 배열에서 제공하는 메서드 중에 filter와 map의 활용경험은?
filter와 map의 공통점은 해당 메소드를 실행하는 배열에 대한 콜백 함수를 적용했을 때 결과 배열을 리턴한다는 것이다. 그리고 가장 큰 차이점은 filter는 콜백 함수 내부 연산을 통해 조건에 만족하는 배열만 리턴 하므로 배열의 길이가 줄어들수도 있는데, map은 연산을 진행하는 배열과 동일한 길이의 배열을 리턴한다는 점이다.

따라서 filter는 이름 그대로 조건에 만족하는 배열의 값들만 '걸러내어' 배열을 만들게 되며, map은 모든 배열값을 사용할 때, 해당 배열값에 특별한 연산을 통해 모든 값을 바꾸고 싶을때 사용하게 된다.

---
### prototype 이 가진 장점은 무엇인가?
프로토 타입은 객체를 확장하고 객체지향적인 프로그래밍이 가능하게 해준다.
또한 코드의 재사용성이 높아진다.
코드의 재사용성하면 생각나는 단어는 상속이다. 클래스의 개념이 없는 자바 스크립트에서는 프로토 타입을 통해 상속하여 코드를 재사용할수있다.

프로토타입에 의한 코드 재사용은 classical 방식과 prototypal 방식이 있다. classical 방식은 new 연산자를 통해 생성한 객체를 사용하여 코드를 재사용 하는 방법이다. 마치 Java에서 객체를 생성하는 방법과 유사하여 classical 방식이라고 한다. prototypal 방식은 리터럴 또는 Object.create()를 이용하여 객체를 생성하고 확장해 가는 방식이다. 두 가지 방법 중 JavaScript에서는 prototypal 방식이 classical 방식보다 간결하게 구현할 수 있다.

---
### prototype 을 통해 객체를 만드는 방법에 대해서 설명하기.
함수를 정의하고 파싱단계에 들어가면 내부에서 수행되는 작업이 있다. 기본적인 함수 멤버로 prototype 속성이 있는데 이 속성은 다른 곳에서 생성된 함수 이름의 프로토타입 객체를 참조한다. 프로토타입 객체의 멤버인 constructor 속성은 함수를 참조하는 내부구조를 가진다. 여기서 알아야하는 부분은 프로토타입 객체는 new라는 연산자로 생성된 모든 객체의 원형이 되는 객체이다.

javascript에서 기본 데이터타입(boolean, number, string, null, undefined)을 제외하고 모두 객체이다. 사용자 정의 함수도 객체이고, new 연산자를 통해 만들어진 것도 객체이다. 객체안에는 proto(비표준) 속성이 있다. 이 속성은 객체가 만들어지기 위해 사용된 prototype 객체를 숨은 링크로 참조하는 역할을 한다.

결론을 내리면, 프로토타입 객체는 새로운 객체가 생성되기 위한 원형이 되는 객체이다. 같은 원형으로 생성된 객체가 공통으로 참조하는 공간이다. 프로토타입 객체의 멤버를 읽는 경우에는 객체 또는 함수의 prototype 속성을 통해 접근할 수 있다. 하지만 추가, 수정, 삭제는 함수의 prototype 속성을 통해 접근해야 한다.

```
function Person(){}

var joon = new Person();  
var jisoo = new Person();

Person.prototype.getType = function (){  
    return "인간";
};

console.log(joon.getType());   // 인간  
console.log(jisoo.getType());  // 인간
```

---
### es6에서 본인이 생각할때 지난번대비 개선된 점은 무엇이고, 왜 그렇게 생각하는지?
기존에 필요성이 대두되었던 부분에 대해서 상당히 많은 발전을 이루었다고 생각한다. 예를 들면 전역 변수에 대한 문제점을 해결하기 위해 let과 const 등의 키워드를 새로 도입한것도 변화의 한 부분이라고 할 수있다. es6의 전반적인 변화에 대해서 보자면 기존에 자바스크립트가 가지고 있던 문제점에 대한 해결과 편의성 증진이 중점이라고 볼수 있다. 앞서 언급한 전역에 대한 처리나, 객체를 생성하는데 사용되는 class, arrow, spread operator, 기본 파라미터 초기값 등은 문제점과 편의성을 해결하기 위해 자바스크립트가 부단한 노력을 통해 변화한다는 것을 알 수 있다. 이는 웹 기술에서 자바스크립트가 거의 표준으로 자리 잡으면서 그에 따른 관심과 사용률이 증가함에 따른 결과라고 생각한다.

---
### event delegation의 원리는 무엇인지? 적용한 경험이 있다면 어떤기능이였는지?
event delegation은 자식 노드에서 발생한 이벤트를 부모가 처리하도록 위임한다. 이는 버블링이라는 특징을 이용한 것인데, 자식 노드에서 발생한 이벤트가 부모노드에 전달되기 때문이다. event delegation이 가지는 장점은 크다. 예를들어 ul>li 태그마다 동일한 이벤트를 적용 시키려면 javascript에서 하나씩 이벤트 리스너를 붙여주어야하는데, event delegation을 이용하면 ul태그, 또는 ul태그의 상위 태그에서 이벤트를 처리해주면 되기 때문이다. 이렇게 이벤트를 구현한다면 해당 부모 노드에 1개의 이벤트 리스너만 필요하게되며 따라서 불필요한 코드가 사라지고 li를 마음껏 늘릴수 있는 확장성도 가지게 된다.

---
### 좋은 코드를 만들기 위해서 노력한 경험들은 무엇인지?
좋은 코드를 만들기 위해서는 시작전의 단계에서는 올바른 설계와, 시작후 단계에서 끊임없는 리팩토링이 필요하다고 생각한다. 올바른 설계를 위해서 백로그를 작성하고 git에 이슈를 등록하여 이에 맞추어 개발을 진행했다. 그러나 코드를 작성하는 과정에서 예상치 못한 기능이나 이슈가 발생하기 때문에 백로그와 이슈를 계속해서 수정하는것이 필요하다. 또한 일정 파트가 완성되었을때 리팩토링을 진행하는데, 본인이 생각했을때 컨벤션에 어긋나거나 수정할수 있는 부분은 즉각 고칠수 있지만, 가장 중요한것은 코드리뷰라고 생각한다. 따라서 일정 기간마다 코드 리뷰를 진행하면서 보다 효율적인 코드로 발전시킨 경험이 있다.

---
### 전역변수를 없앨 수 있는 방법들은 무엇인가?
가장 효과적인 것은 namespace 패턴을 이용하여 파일을 모듈화 하면, 해당 함수나 변수를 사용하기 위해서
네임스페이스의 경로가 붙기 때문에 변수와 함수 이름의 충돌이 방지된다.
또한 생성자 함수를 사용하거나 es6에서 추천하는 let 변수 타입를 사용하는 것도 방법이 될수 있다.

---
### 이벤트를 거쳐 API를 통해 dom조작까지 이어지는 과정을 순서대로 설명해보라.
1. 이벤트 리스너 함수를 통해 web API에 해당 이벤트 콜백 함수가 등록된다.
2. 해당 이벤트 실행 조건이 발동 되면 event queue에 들어가게 되고 call stack이 빌때까지 대기한다.
3. call stack이 비면 stack에 들어가 함수가 실행된다.
4. 만약 콜백 함수가 dom 조작을 한다면 dom tree에 접근한다.
5. root에서부터 내려와 타겟 dom에 접근하여 dom 조작을 마치고 이벤트가 종료된다.


---
### setTimeout을 이용해 재귀호출을 하는 경우 어떤 장점이 있는가?
설정된 시간마다 해당 함수가 반복되면서 별도의 처리 없이 해당 파트를 새로고침할수 있게 된다.

---
### 문제가 있을때 본인이 가장 자주 사용하는 디버깅 과정은 무엇인가?
좋은 방법은 아니지만 console.log를 통해서 해당 함수안에 진입하고 있는지, 또는 변수가 제대로 할당되었는지 찾아볼 때가 있다. 별도의 조작 없이 빠르게 알아 볼수 있기때문에 단편적인 기능이 잘 동작하고 있는지 확인할 때 사용한다. 만일 이와 같이 작은 기능이 아니라 변화를 보기 위해서는 구글 개발자 도구를 이용해서 브레이크 포인트를 설정하고 해당 변수가 잘 할당되는지, 함수가 제대로 동작하는지 찾아본다.

---
### github을 통해서 협업과정을 거치는 과정을 branch를 중심으로 설명하기.
기본적으로 master branch는 조작하지 않는다. master branch에 merge가 이루어지는 시점은 major 기능에 대한 작업이 끝나고 release될 때로 설정한다. 따라서 master branch에서 dev와 같은 별도의 브랜치를 만들어 작업한다. 만약 기간에 나누어 스프린트 작업을 한다고 하면 마일스톤에 목표들을 등록하고 목표일_ milestone과 같은 브랜치를 dev로 부터 다시 만들어 작업한다. 이 때 milestone에서 나오는 branch는 기능별로 구현하고 다시 milestone으로 merge한다. 해당 기간이 끝나는 시점에 dev로 milestone branch를 merge한다. 

---
### jQuery를 사용하는 것의 장점과 단점은 무엇이라고 생각하는지.
jQuery의 슬로건은 write less, do more이다. 슬로건에 걸맞기 기존 자바스크립트에서 사용하는것 dom 조작 코드보다
압도적으로 짧은 코드를 자랑한다.
또한 멀티 브라우저 지원으로 다른 브라우저 환경이라도 동일한 동작을 하는것이 특징이다(브라우저 호환성).

단점은 jQuery를 사용하기 위해서 새로운 API를 학습해야하는 수고로움이 동반된다.
또한 어플리케이션 마다 다른 요구사항에 최적화 하기 위해서 jquery자체에 직접 파고 들어하는 경우가 생길수 있다.
그리고 코드가 짧기때문에 평소보다 많이 붙이게 되고 가독성이 떨어져 코드관리가 어렵다.
마지막으로, jQuery의 용량 문제이다. 한두개의 기능을 사용하기 위해서 jquery의 거대한 용량을 사용하는 경우라면
상당히 비효율적이라고 할 수있다.
즉 가장 큰 문제는 속도라고 할 수있다.

extra
멀티 브라우저의 호환성 문제는 대부분의 브라우저가 html5와 es6를 지원하고 있기 때문에 호환성문제는 크게 개선되는 중이다.

---
### 정규표현식으로 email을 체크해보기.

```
var regExp = /^[0-9a-zA-Z]([-_.]?[0-9a-zA-Z])*@[0-9a-zA-Z]([-_.]?[0-9a-zA-Z])*.[a-zA-Z]{2,3}$/i;
```

---
### 요즘 관심있게 지켜보는 라이브러리나 오픈소스가 있다면 무엇인지? 어떤점이 마음에 드는지?
페이스북에서 개발중인 리액트JS에 대해서 관심이 많다. 현재 웹 트랜드가 SPA(single page web application)으로 변화하면서 전통적으로 서버에서 처리하던 랜더링을(server side rendering) 클라이언트 사이드에서 처리해주는 방식으로 변화했다. 왜냐하면 싱글 페이지의 경우 페이지가 로딩될때마다 서버에서 렌더링을 한다면 트래픽이 과다하게 초과되기 때문에 비효율적이기 때문이다. 그러나 서버에서 JSON 으로 파일만 보내준다면 클라이언트 사이드에서 렌더링을 진행하게 된다. 이러한 트렌드에 맞추어 등장한것이 angular, backbone, react 등이다. react는 angular와 backbone과 다르게 프레임 워크가 아닌 라이브러리이다. react는 virtual dom을 이용해서 클라이언트 사이드 렌더링을 진행하게되는데, 바뀐 내용이있을 때 마다 자동으로 실행되므로 편리하다는 장점이 있다. 또한 es6의 문법을 이용하기 때문에 최신화되었고 컴포넌트 단위로 관리 하므로 재사용성이 높다는것이 마음에 든다.

---
### 서비스 성능개선을 했던 사례를 말해보자.

---
### this 에 대해서 설명하기.
this는 문맥(context)을 가리킨다. 현재 영역이 어디인가, 호출자가 누구인가 등을 가리키며, 조건과 스코프에 따라서 변경된다.
따라서, this는 유동적이며 가변적이라고 할 수 있는데 조건은 아래와 같다.

- 기본적으로 this는 global 객체이다. 
- function 영역에서의 this는 부모 객체이다. 단, 그 부모의 자식으로서 불렸을 때에만. 
- new 연산자로 생성된 function 영역의 this는 새로 생성된 객체 그 자신이다. 
- call 혹은 apply로 호출 된 함수의 경우 call, apply의 첫번째 인자로 명시 된 객체이다. 

---
### this를 변경시킬 수 있는 방법을 코드로 예시로 보여주기.
this는 call과 apply, bind로 변경할 수 있다. 3가지 메소드의 차이점은 다음과 같다.

- call : context를 변경, 인자를 인수로 전달
- apply : context를 변경, 인자를 배열로 전달
- bind : context를 변경

call과 apply는 prototype으로 정의된 함수를 빌려와서 사용하는데 컨텍스트를 묶어주는데 사용할수 있기때문에 유사배열인 arguments에 배열의 메소드를 적용할때 사용된다. bind는 함수를 호출하지 않고 현재의 컨텍스트를 전달할때 사용된다.

##### [예제 1]
```
var obj = {
  string: 'zero',
  yell: function() {
    alert(this.string);
  }
};
var obj2 = {
  string: 'what?'
};
obj.yell(); // 'zero';
obj.yell.call(obj2); // 'what?'
```

##### [예제 2]
```
var obj = {
  string: 'zero',
  yell: function() {
    alert(this.string);
  }
};
var obj2 = {
  string: 'what?'
};
var yell2 = obj.yell.bind(obj2);
yell2(); // 'what?'
```
---
### bind 메서드의 내부 코드는 어떻게 됐을까?

---
### IE9 지원이 필요하지만, ie9 에서 제공하지 않는 최신 javascript API를 사용하고 싶을때, 어떻게 대처할 것인가?

---
### 팀장님이 내가 전혀 모르는 기능에 대한 개발을 부탁하면 어떻게 대응할 것인가?

---
### 모듈패턴은 어떻게 구현할수 있는지? 모듈패턴의 어떤 장점이 있는지?
자바스크립트에서는 public이나 private에 대한 별도의 키워드를 제공하지 않는다. 따라서 객체 생성시 모든 변수에 접근할 수 있게 되는데
이때 클로저를 이용해서 객체를 생성하게 된다면 내부 변수에 대한 접근이 리턴된 함수에 대해서만 접근할수 있게 된다. 자연스럽게 이를 위해 setter, getter를 만들어야한다. 모듈패턴을 사용하게 되면 public과 private의 특성을 자바스크립트에서 사용하게 되며 이에 따른 장점도 따라오게 된다.

```
var testModule = (function () {
  var counter = 0;

 return {
       incrementCounter : function() {
             return ++counter;
       },

       resetCounter : function() {
            console.log("counter value prior to reset: " + counter);
            counter = 0;
       }
 };
})();

testModule.incrementCounter(); // 1
testModule.incrementCounter(); // 2
testModule.incrementCounter(); // 3
testModule.incrementCounter(); // 4
testModule.incrementCounter(); // 5
testModule.incrementCounter(); // 6
testModule.resetCounter(); //"counter value prior to reset: 6"
```
---
### javascript 코드를 html하단에 주로 배치하는 이유는 ?
 javascript는 주로 dom 조작을 하기 위해서 사용된다. html은 코드 상단에서 부터 랜더링 되며,
 때문에 javascript 코드가 html 상단에 위치해있다면 랜더링이 완료되기도 전에 dom content를 호출하게된다.
 결과적으로 호출된 dom content는 undefined값을 가지기 때문에, 하단에 자바스크립트 코드를 배치하는 것이다.

---
### javascript 코드를 여러개 html에 추가하는 것과, 하나로 머지하여 배포하는 것의 장단점은 무엇인가?

---
### html을 내려받으면서 브라우저가 화면에 모든것을 표현하기까지의 전체 렌더링 과정을 설명해보자.
브라우저의 주요 기능은 사용자가 선택한 자원을 서버에 요청하고 브라우저에 표시하는 것이다. 이를 위해서 각 브라우저마다 고유의 랜더링 엔진을 사용하게 된다.

1. DOM 트리구축을 위한 HTML 파싱
2. 랜더 트리 구축
3. 랜더 트리 배치
4. 랜더 트리 그리기

렌더링 엔진은 HTML 문서를 파싱하고 "콘텐츠 트리" 내부에서 태그를 DOM 노드로 변환한다. 그 다음 외부 CSS 파일과 함께 포함된 스타일 요소도 파싱한다. 스타일 정보와 HTML 표시 규칙은 "렌더 트리"라고 부르는 또 다른 트리를 생성한다.렌더 트리는 색상 또는 면적과 같은 시각적 속성이 있는 사각형을 포함하고 있는데 정해진 순서대로 화면에 표시된다.
렌더 트리 생성이 끝나면 배치가 시작되는데 이것은 각 노드가 화면의 정확한 위치에 표시되는 것을 의미한다. 다음은 UI 백엔드에서 렌더 트리의 각 노드를 가로지르며 형상을 만들어 내는 그리기 과정이다.
일련의 과정들이 점진적으로 진행된다는 것을 아는 것이 중요하다. 렌더링 엔진은 좀 더 나은 사용자 경험을 위해 가능하면 빠르게 내용을 표시하는데 모든 HTML을 파싱할 때까지 기다리지 않고 배치와 그리기 과정을 시작한다. 네트워크로부터 나머지 내용이 전송되기를 기다리는 동시에 받은 내용의 일부를 먼저 화면에 표시하는 것이다.

---
### ecmascript란 무엇인가?
 자바스크립트와 ecmascript는 다르다. 자바스크립트(Javascript)가 넷스케이프(Netscape) 브라우져만이 아니라 다른 웹 브라우져들의 지원까지 받기 시작하면서 다양한 웹 브라우져에서 자바스크립트(Javascript)가 공통되게 잘 작동하기 위해서 표준 규격이 필요해졌는데, 이 때문에, ECMA 국제 기구에서 "ECMAScript Standard"라 불리는 스크립트 표준이 만들어지게 된다. 자바스크립트와 비슷한 뜻으로 많이 들어보았을텐데, Javascript는 ECMAScript와 BOM(Browser Object Model) 와 DOM(Document Object Model)이라는 1개의 코어와, 2개의 모델로 이루어져 있다. 즉, 흔히 우리가 자바스크립트(Javascript)라 부르는 것은 정확히 말하면 3가지가 합쳐서 만들어진것인데 그것들은 바로 ECMAScript 와 DOM(Document Object Model) 와 BOM(Browser Object Model) 이다

 ECMAScript는 자바 스크립트를 이루는 코어(Core) 스크립트 언어로, 웹 환경에서만 호스트 되는 언어가 아니다. 웹 환경은 ECMA 스크립트가 호스트되는 환경들 중 하나일 뿐이다. EMCA 스크립트 호스트 환경은 ECMA 스크립트 실행 환경이 구현되있고, 각각 그 환경에 알맞는 확장성을 가지고 있다. 예를들어 웹 브라우져 환경에서는 BOM(Browser Object Model)과 DOM(Document Object Model)이 그 확장성이 되겠다. 이러한 확장성들은 EMCA 스크립트의 문법과 기능에 맞춰 기능의 확장을 가능게 한다. 자바스크립트의 document 객체가 좋은 예이다. 다른 호스트 환경으로는 node.js, Adobe Flash, MongoDB, CouchDB  등이 있다

 ECMA 스크립트는 기본적으로 언어의
- 문법(Syntax)
- 데이터 타입(Type)
- 구문(조건문, 반복문 등)(Statement)
- 키워드(Keyword)
- 예정 키워드(Reserved Word)
- 연산자(Operator)
- 객체(Object)
등을 규정짓는다. 이는 어떤 ECMA 스크립트 호스트 환경에서든 동일하다.

---
### 코드리뷰를 했던 사례를 말해보라. 어떤점을 느꼈는가?
HTML canvas를 이용해서 테트리스 게임을 만드는 작업을 협업을 통해 진행했다. 나는 profile과 ranking 출력 파트를 맡아서 진행했는데 네임스페이스나 생성자 없이 코드를 짜게되었다. 그러나 코드 리뷰를 통하여 생성자 함수를 이용해 리팩토링 하게 되었고 코드가 좀더 모듈화 되고 눈에 잘 들어오게 되었다. 또한 코드리뷰를 반복할 때 마다 함수의 분리나 변수 네이밍 등을 수정하면서, 효율적인 코드로 변하는것이 느껴졌다. 결론적으로, 자신이 혼자 작업하면 눈에 잘 들어오지 않는 코드들이 다른 사람의 리뷰를 통해서 좀더 좋은 코드로 개선되고 효율적으로 변해가는 것을 느꼈다.

---
### DOM Tree란 무엇인가?
브라우저가 HTML을 전달하면 브라우저 랜더 엔진이 이를 파싱하고 DOM 노드로 이루어진 트리 구조를 만든다. 이 때 각 노드는 각 HTML 엘리먼트들과 연관되어있다. 따라서 사용자는 DOM TREE에 접근하여 DOM조작을 할 수 있게된다.

---
### innerHTML을 직접 구현하면 어떻게 구현해야 할까?

---
### 유니크한 데이터를 집합으로 가지는 set을 array 로 구현하면 어떻게 구현할 수 있을까?
indexOf 함수로 해당 데이터를 검색한 후 배열 내부에 데이터가 존재하면 바꾸어주는 방식으로 구현이 가능하다.

---

### touch 이벤트와 mouse이벤트의 차이점은 무엇인가?

---
### preventDefault는 언제 쓸 수 있는 것인지?
현재 이벤트의 기본동작을 중지한다. 상세하게 이야기하면 이벤트외의 별도의 브라우저 행동을 막기 위해 사용된다.
예를 들어, a태그를 사용하게 되면 2가지의 기능이 실행되는데 1. 클릭 이벤트를 실행하고, 2. href에 표시된 곳으로 이동한다.
따라서 클릭 이벤트만 실행하기 위해 preventDefault를 사용할 수 있다. 글을 작성할 때나 회원가입 버튼을 클릭 했을때 페이지가 위로 쭉 올라가는것을 방지할 수있다.

---
### 버블링과 캡처링을 설명하세요.
- 버블링 : 자식 노드에서 발생한 이벤트가 부모 노드로 전달된다.
- 캡쳐링 : 부모 노드에서 발생한 이벤트가 자식 노드로 전달된다.
버블링과 캡쳐링은 addEventListener의 세번째 인자로 설정할수 있으며 버블링은 (false) 캡쳐링은 (ture)가 된다.
stoppropagation 함수를 이용하면 버블링과 캡쳐링을 차단할 수있다.

---
### 배포나 릴리즈 전에 코드를 어떻게 테스트 할 수 있는지? 좋은 사례나, 경험을 말해보기.

---
### 콜백함수란 무엇인지 설명하기.
함수내에 인자로 넘겨진 함수를 콜백 함수라고 한다. 콜백함수는 조건을 만족하면 언제든 원하는 시점에 실행시킬수 있다. 대부분 비동기로 실행되며, 싱글 스레드인 자바스크립트에서 필수적으로 사용되는 기능이라고 할 수 있다. 주로 이벤트나 ajax 처리 등에 사용된다.

---
### template 을 어떻게 관리하는 게 좋다고 생각하는지 ?
서버 사이드 랜더링을 할 경우 템플릿 엔진을 사용해서 별도의 템플릿만 구현하는 것이 좋다. 클라이언트 랜더링을 할 경우 HTML에 template 양식을 만드는 방법이 있는데, 이는 관리하기 어렵고 불필요한 코드가 들어가게 된다. 따라서 es6에서 제공하는 템플릿 기능을 사용해서 js파일 내부에 네임스페이스 안에서 관리하는게 좋다.

---
### 자바스크립트에서 빌드는 어떤 것을 하는 것일까? 사용해본 도구가 있는지?

---
### 팀프로젝트에서 제일 중요한 부분은 무엇이라고 생각하는가?
팀프로젝트에서 가장 중요한것은 컨벤션과 커뮤니케이션이라고 생각한다. 서비스를 여러명이서 만드는 것보다 한명이 빠르게 완성하는게 가장 좋지만 이는 비현실적이므로 팀원들과 협업을 진행하게 된다. 그러나 여러명이 프로젝트를 진행하다보면 각자 코딩 스타일과 지향하는 목표가 다르기 때문에 올바르게 팀프로젝트가 진행되기 어렵다. 따라서 컨벤션을 확립하고 끊임없는 커뮤니케이션을 통해 한사람이 작성한 코드처럼 일관성있는 프로그래밍을 지향해야한다. 커뮤니케이션은 많으면 많을수록 좋다고 생각한다.

---
### 커뮤니케이션을 잘하기 위해서 어떤 방법을 해보았는가?
slack을 통한 소통, git scrum wiki 등록, 페어 프로그래밍, 하루 회고, 페어프로그래밍, 팀 회의를 진행했다.

---
### 커밋로그가 가진 의미는 어떤것일까? 어떤 규칙이 좋다고 생각하는지?
커밋은 저장의 측면에서 코드의 히스토리, 기록이라고 할 수 있다.
주석이 정적인 소스에 대한 설명을 담는다면 커밋로그는 변화되거나 추가된 코드들에 대한
주석이라고 볼수 있다. 따라서 자신이 작성한 코드의 변경사항을 한눈에 보거나, 타인에게 자신이 변경한 코드의 내용을
여러줄에 걸쳐 설명할 때 사용하게 된다.

때문에 가독성이 좋고 명시적이며, 규칙적인 커밋로그가 좋다.
git에서 추천하고 있는 명령형 어조나 개행의 규칙을 지켜야하며
개인적으로는 개조식으로 표현하여 보는 사람이 한눈에 커밋의 로그를 확인할수 있도록 하는것이 좋다고 생각한다.

---
### less , sass를 써보았는가? 그것이 가진 장점은 무엇인지? 왜 그런것이 나왔다고 생각하는지?

---
### feature detection에 대해서 설명하시요.

---
### 모바일웹의 애니메이션 구현에 대한 경험과 가장 좋은 방식을 말해보세요.

---
### 웹화면에 가운데 정렬이 되는 모달다이얼로그를 어떻게 구현할 수 있을까?

---
### 검색자동완성을 위한 수도코드를 작성해보세요.

---
### merge 과정에서 생기는 충돌을 해결하는 과정을 설명하세요.
우선 merge에 의한 충돌은 브랜치를 병합할 때 생기게 된다.
세부적으로 merge는 원격에서 발생하는 경우와 로컬에서 발생하는 경우가 있다.

로컬에서 발생하는 경우는 대개 작업 범위가 개인인 경우가 많으므로 충돌이 일어난 소스를 찾아
base와 compare중 적절한 코드로 적용해준다.

원격에서 발생하는 경우는 pull request가 auto merge되지 않을 때이다.
이때는 병합하려는 base 원격 브랜치를 pull을 이용해 로컬로 가져 온 뒤 충돌을 로컬에서 해결해주고,
다시 pull request를 보내서 원격 레파지토리에서 merge를 요청한다.

---
### REST API는 무엇인가?
REST API는 웹의 창시자인 Roy Fielding이 2000년 논문에서 소개했다. 그는 "현재 웹서비스들이 HTTP의 본래 의도와 우수성을 제대로 활용하지 못하고 있다"고 지적하면서 웹의 장점을 최대한 활용할 수 있는 네트워크 기반의 아키텍처로 REST를 제안했다. REST API의 장점으로는 "Easy to learn, Easy to use, hard to misuse"라는 슬로건에 걸맞게 사용하기 쉬우나 잘못 쓰기 어려운 이다. REST는 아키텍쳐 스타일이므로 이 스타일을 강하게 규제하지 않는다. 따라서 RESTful API라는 말을 많이 사용한다.
REST API란 Representational State Transfer(표현 상태전이)의 약자이다. REST API는 크게 리소스, 메서드, 메세지로 이루어져있다. 

- 리소스 : "사용자" -> "http://myweb/user" 라는 형태의 URI
- 메서드 : "생성한다"라는 행위 -> HTTP POST 메서드
- 메세지 : "이름이 tom인 사용자" -> 생성하고자 하는 사용자의 내용은 JSON 문서를 이용해서 표현

##### 리소스
- 동사를 지양하고 명사형을 사용한다.
- 단수보다 복수형을 사용한다.
- 일관된 케이스를 사용한다.(카멜, 언더바, 헝가리안)
- 메서드와 end-point만 보고 무엇을 하는것인지 알수 있어야한다.

##### 메서드
- POST : 등록/Create
- GET : 조회/Select,Read
- PUT : 수정/Update
- DELETE : 삭제/Delete

---
### post와 get의 차이점을 설명하세요.
http post와 get은 서버에 무엇을 전달할 때 사용하는 통신 방식이다.
1. get은 주소줄에 parameter가 붙어서 전송되지만 post는 http body 안에 전송된다.
2. get은 보낼수 있는 parameter의 길이가 한정되어있지만 post는 body안에 보내지므로 용량이 더 크다.
3. RESTful API의 관점에서 get은 가져오는 것이고 post는 수행하는 것이다.

1번 때문에 get은 최소한의 보안도 유지되지 않으나, post는 그나마 parameter의 숨김이 가능해진다. 하지만 보안적으로 둘다 안전하지는 않다. 또한 post방식은 body 안에 보내지므로 클라이언트에서 인코딩하고 서버에서 디코딩 하는 시간떄문에 get에 비해 상대적으로 처리 속도가 늦다.
3번이 가장 중요한 차이점이라고 할 수 있는데, get은 server내의 데이터 변경 없이 조회 등의 기능을 수행할 때 사용되며, post는 server의 상태나 데이터를 변경을 위해 사용된다.

---
### http header는 무엇인가요?
HTTP 헤더는 클라이언트와 서버 사이에서 모든 종류의 정보를 전송하는데 이용되며 크게 요청(request) 헤더/ 응답(response) 헤더로 분류할 수 있다. 헤더에는 HTTP 요청을 식별할 수있는 메타데이터가 들어가게된다. 헤더에 들어갈 수 있는 내용은 아래 4개와 같다.

- General : 클라이언트, 서버 또는 HTTP와 관계된 정보
- Request : 문서 양식과 서버의 매개 변수들
- Response : 응답을 보내는 서버에 대한 정보
- Entitiy : 클라이언트와 서버 사이에 전송되는 데이터에 대한 정보

---
### javascript의 call stack에 대해서 설명하세요.
자바스크립트는 싱글 스레드 기반의 언어로써 하나의 콜스택을 가진다. 자바스크립트 코드가 실행되면 인터프리터는 코드를 해석하게되는데, 이때 처리해야할 함수 등이 실행되면 해당 문맥(context)를 콜스택에 가져온다. 콜스택은 이름에서도 알수 있듯이 스택(stack) 자료구조이므로 LIFO(Last In First Out)의 구조를 가지며, 때문에 나중에 들어온 함수부터 실행되게 된다.
예를 들면, 함수내에서 함수를 실행할 경우 나중에 실행된 함수가 콜스택 가장 위에 쌓여 먼저 실행된다. 비동기 함수의 경우 task queue에서 대기하다가 콜스택이 비어 있을 경우(main context까지 실행된 후) 앞에서부터 꺼내져 스택에서 실행된다.

---
### 비동기 함수안에 비동기 로직이 또 있을때 이를 어떻게 보기 좋게 해결할 수 있을지 사례와 원리를 설명하세요.
비동기 함수를 처리한 결과값으로 비동기 로직을 처리할 때, 이와 같은 로직이 다수로 중복되게 되면 피라미드 구조를 나타내며 콜백 지옥을 만날수 있다. 이러한 상황을 극복하기 위해 promise라는 패턴이 제안되어왔다. promise패턴을 사용할 경우 장점은 다음과 같다.

- 비동기 작업들을 순차적, 병렬적으로 처리하며 컨드롤이 수월해진다
- 코드의 가독성이 좋아진다.
- 예외처리에 대한 구조가 탄탄하기 때문에 오류가 발생했을 때 가시적으로 관리할 수 있는 장점이 있다.

##### [promise 선언부]
```
//Promise 선언
var _promise = function (param) {

	return new Promise(function (resolve, reject) {

		// 비동기를 표현하기 위해 setTimeout 함수를 사용 
		window.setTimeout(function () {

			// 파라메터가 참이면, 
			if (param) {

				// 해결됨 
				resolve("해결 완료");
			}

			// 파라메터가 거짓이면, 
			else {

				// 실패 
				reject(Error("실패!!"));
			}
		}, 3000);
	});
};
```
promise는 말그대로 약속이다. "현재는 값이 없는데 이후에 콜백이 발생하면 결과값을 주고 이상이 있으면 알려준다"는 뜻이다. 따라서 promise는 다음과 같은 상태중에 하나가 된다.
1. pedding : 아직 약속을 수행 중인(fulfilled 혹은 reject되기 전) 상태이다.
2. fulfilled : 약속이 지켜진 상태이다.
3. reject : 약속이 어떠한 이유에서 못지켜진 상태이다.
4. settle : fulfilled이건 reject이건 결론이 난 상태이다.

위의 선언부를 보면 나중에 promise 객체를 생성하기 위해 promise 객체를 리턴하도록 함수록 감싸고 있다. promise 객체만 보면 파라메터로 익명함수를 담고 있고, 익명함수는 resolve와 reject를 파라메터로 받고 있다. 이 후 비동기 작업이 마친뒤 결과물을 약속대로 잘 줄수 있다면 첫번째 파라메터로 주입 되는 resolve 함수를 호출하고, 실패했다면 두번째 파라메터로 주입되는 reject 함수를 호출하는 것이 promise의 주요 개념이다.

##### [promise 실행부]
```
//Promise 실행
_promise(true)
.then(function (text) {
	// 성공시
	console.log(text);
}, function (error) {
	// 실패시 
	console.error(error);
});
```
_promise를 호출하면 Promise 객체가 리턴된다. Promise 객체에는 정상적으로 비동기 작업이 완료되었을 때 호출하는 then이라는 API가 존재한다. 위의 예제에는 하나의 then API를 호출해서 비동기 작업이 완료되면 결과에 따라서 성공이나 실패 메세지를 콘솔로그로 찍어주게 된다.

then API는 첫번째 파라메터에 성공시 호출함수를, 두번째 파라메터에 실패시 호출할 함수를 선언하면 Promise의 상태에 대해 수행하게 된다. 앞서 선언부에서 Promise 객체를 생성할때 resolve와 reject 파라메터를 받았는데 그 파라메터가 실행부의 함수와 동일하다.


##### [promise 에러처리]
```
_promise(true)
	.then(JSON.parse)
	.catch(function () { 
		window.alert('체이닝 중간에 에러가!!');
	})
	.then(function (text) {
		console.log(text);
	});
```
만약 체이닝 형태로 연결한 비동기 작업에서 에러가 발생하면 위와 같이  catch문을 사용하여 에러를 해결할 수 있다.

---
### 네임스페이스 패턴의 장점은?
대한민국에 사는 '홍길동'이라는 사람을 찾는다면 이름만으로는 찾을수가 없다. XX시 XX구 XX동 이라는 구체적인 지번이 있으면 좀더 쉽게 찾을 수있다. 이처럼 원하는 결과를 쉽게 찾기 위한 번지의 역할을 하는 것이 네임스페이스이다. 결국 네임 스페이스는 객체나 변수가 겹치지 않는 안전한 소스코드를 만들기 위해서 사용된다. 따라서 다음과 같은 장점을 가진다.

- 계층적으로 의미에 맞춰서 기능들을 그룹화 할 수 있다.
- 해당 기능을 어디서 호출하는지 혼란스럽지 않다. 유지보수에 용이하다.
- 전역변수를 획기적으로 줄일 수 있다.

---
### react, vue, angular라이브러리 중 하나를 골라야할때 어떤식으로 고를 예정인가요?

---
### 개발시 어려움이 많거나 풀리지 않을경우 어떤 해결방법을 사용하는가?
새로운 기술에 대한 개발을 진행할 때 다음과 같은 순서로 작업을 하게 된다.
1. 먼저 해당 기술의 공식 문서를 참조한다.
2. slide share에 올라간 강의 프레젠테이션을 보면서 학습한다.
3. github에서 예제 코드를 참조한다.
4. google 검색을 통해 해당 기술에 대해 찾아본다.
5. 관련 기술을 주제로한 도서를 찾아본다.
6. 다음에 같은 기능을 구현할 경우가 있으므로 기록으로 남겨둔다.
이와 같은 프로세스로 진행하게 된다면 어려움없이 진행되는 경우가 많다.
그럼에도 불구하고 잘 풀리지 않을경우 우선 해당 기능의 우선순위를 뒤로 미루어놓고 다른 기능을 먼저 구현한다.
그리고 다시 돌아왔을 때 잘 풀리는 경우가 많다.

---
### 배워나가는 기술을 공유하거나 기록하는 것들이 있는지?
네이버와 티스토리 블로그 운영 중,
git에 개인 스터디 레파지토리를 만들어 자료 저장 중

---
### 본인이 생각하는 가장 적절한 커밋단위는 ?
가능한 세세하게 나누어 자주 커밋하는것이 좋다고 생각한다.
예를 들면 기능(feature) 단위로 나누는 것도 방법이 될수 있고, function 구현이 완료되면
커밋 하는 것도 방법이 될수 있다.
git의 가장 강력한 기능중의 하나로 예전의 상태로 돌아가는 것을 꼽을수 있는데, 커밋을 이용해
많은 분기점을 만들어 놓으면 많은 코드를 날리지 않고 되돌릴수 있는 장점이 있다.
즉, 커밋은 소스 코드 저장의 측면에서 히스토리로 남기 때문에 기능 단위의 세밀한 커밋단위를 지향한다.

---
### 디자이너와 기획자가 구현이 불가능할 것으로 예상되는 기능개발을 요구할때 대처방법은?

---
### front-end 개발자의 역할은 어디까지 일까?

---
### nodeJS의 설치방법과 모듈화를 통한 웹서버 라우팅을 구현할 수 있다.
가능하다.

---

## 참조목록
   1. [게으른 개발자 블로그](http://lazydev.tistory.com/)
   2. [DailyEngineering blog](https://hyunseob.github.io/) 
   3. [Unikys blog](http://unikys.tistory.com/)
   4. [yubylab blog](http://yubylab.tistory.com/) 
   5. [jui blog](http://blog.jui.io/)