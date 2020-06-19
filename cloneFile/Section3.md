- css의 3가지 핵심
  - 반응형 디자인, 유지관리 및 확장가능형 코드, 웹 성능



- 웹페이지가 Load되는 과정에서 CSS도 Parse되며 DOM과 같이 CSSOM이라는 object model로 만들어진다.
  이후 DOM과 CSSOM을 통해 Render treer가 구성된다.

![스크린샷 2020-06-19 오후 1.11.03](/Users/pch/Library/Application Support/typora-user-images/스크린샷 2020-06-19 오후 1.11.03.png)





- CASCADE: 서로다른 declaration으로 인해 충돌이 일어난 경우

  - Author, User, Browser에 의해서 일어남
  - 해결방식 IMPORTANCE > SPECIFICITY > SOURCE ORDER
  - !importat를 속성이 붙어있는것 먼저

  ![스크린샷 2020-06-19 오후 1.21.07](/Users/pch/Library/Application Support/typora-user-images/스크린샷 2020-06-19 오후 1.21.07.png)

  - SPECIFICITY: 아래 순서대로 개수를 세서 같으면 하위 항목의 개수를 비교하는 방식으로 declaration 결정

  ![스크린샷 2020-06-19 오후 1.24.20](/Users/pch/Library/Application Support/typora-user-images/스크린샷 2020-06-19 오후 1.24.20.png)

  - 다같으면 코드의 순서를 통해 결정

- !Important는 정말 중요할때만 사용할것
- Inline style은 우선순위가 제일 높다



- :hover와 같은 효과를 얻기 위해서도 우선순위가 높아야 적용된다.



- CSS 6단계 처리과정

![스크린샷 2020-06-19 오후 3.11.37](/Users/pch/Library/Application Support/typora-user-images/스크린샷 2020-06-19 오후 3.11.37.png)

- 아무것도 declared 하지 않아도 기본 값으로 채워짐(3단계에서)
- browser default가 있으면 2단계에서 cascading이 일어나서 값이 결정됨
- rem단위는 root fontSize에 해당 값을 곱해서 px로 나오게 만듬
- 폰트크기의 %는 부모의 computed value를 기준으로 계산되고, 길이의 %는 부모의 width를 기준으로 계산됨
- 폰트크기의 em은 부모의 폰트크기를 기준으로 계산되고, 길이의 em은 자신의 폰트크기를 기준으로 계산된다.
- 폰트크기를 통해서 길이를 조절하면 보다 좋은 반응형 웹을 만들 수 있음



- 상속과정

  1. 무조건 있어야 하는 css값들을 확인

  2. cascaded 값을 확인

     있다: Specified value는 cascaded 값

     없다: 상속받을 값이 있는가?

     ​	있다면 specifed value는 Computed value of parent element(%등을 px로 계산한 후의 값)

     ​	없다면 초기값으로 설정



- rem은 IE9 이전에서는 지원 안됨



- box model: 요소들이 보여질 공간

- box type: block: box model 적용됨 - Inline-block: box model적용도 되면서 다음줄로 넘어가지 않음 - Inline: 다음줄로 넘어가지 않음

- positioning: 

  - noraml flow

  적혀있는 그대로 layout됨

  - Floats 

  noraml flowwprj

  다른 요소의 옆에 붙게 만듬

  텍스트/inline emlemnt가 floats 주위를 감싸게 됨

  - Absolute

  주변의 요소들에 영향을 받지 않음

  stacking context가 가능해질 수 있음(Z-Index)



- Layout Thinking 3-step

  - Think

    - 모듈화된 블럭구조로 interface를 구성한다.
    - 다른 프로젝트에서도 사용할 수 있게 재사용성있게 구성한다.
    - 어느 페이지에서나 사용할 수 있게 독립적으로 만들어라

  - Build(다양한 방법이 존재)

    - BEM방식을 사용 - HTML에서
      - --: modifier
      - __:element
      - block은 그대로 둠

  - ARCHITECT

    - 7-1Pattern을 사용

    ![스크린샷 2020-06-19 오후 5.04.40](/Users/pch/Library/Application Support/typora-user-images/스크린샷 2020-06-19 오후 5.04.40.png)