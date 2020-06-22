 

### 2

- 7-1을 사용해서 partials and imports
- 폴더를 만들고 내부에는 _로 시작되는 부분파일을 만듬 이후 main.scssdp import
- base
  - 보일러 플레이트와 같이 기존 프로젝트의 difinition을 저장
- abstricts
  - 함수, 변수, mixins등을 저장
  - 프로젝트에서 사용되는 Sass도구와 헬퍼(이것만으로는 css를 산출하지 않아야함)
- components
  - 재사용 가능한 블럭들을 저장
  - 위젯들에 초점
- layout
  - global footer, header 등 내용 저장 사이트나 어플리케이션의 레이아웃에 기여하는 모든것들
  - 거시적 관점
- pages
  - 페이지에 한정된 스타일을 정해둠
- 테마폴더 + vendor(외부 코드 인용)폴더 등이 있음



### 3

- 반응형 디자인
  - Fluid grids and Layouts
  - Flexible Responsive Image
  - Media queries
- 기존의 방식은 float layout방식을 사용했지만 현대에는 Flexbox와 css grid를 사용함
  - flex는 2차원 그래프에서 사용하기 좋음
  - 하지만 이러한 새로운 방식은 browser가 지원해주지 않는다면 큰 문제를 발생시킴



### 4

- block을 가운데 정렬하고 싶으면 margin: 0 auto;를 통해서 가능
- &:not(:last-child)를 통해서 제일 마지막을 제외하고 css를 적용시키도록 할 수 있음 -> pseudo를 사용하는것보다 좋음
- sass 변수를 calc에서 사용하기 위해서는 #{ }으로 감싸주어야함
- ['내부속성' = "속성 값"] {} 을 통해 내부 속성에 해당되는 선택을 할 수 있음
  - 이때 ^=는 속성값으로 시작하는 요소만 선택
  - *=는 내부에 속성값이 존재하는 모든 요소들을 선택
  - $=는 속성값으로 끝나는 모든 요소들 선택





### 5

- .클래스이름 을 통해 자동으로 div class명까지 생성(.앞에 요소 이름을 넣으면 다른 요소들이 생성됨)
- utility 를 사용하는 이유는 재사용성을 유지하면서 element에 필요한 설정(text-align, margin-bottom)을 해주기 위해서이다.
- 자식 요소를 만뜰고 싶을때는 .클래스이름>.클래스이름을 사용하면 된다.
- *3과 같은 곱셈 연산을 통해 자식을 여러개 추가할 수 있음



### 7

- 가능하면 이미지의 너비는 백분율로 표시하라 -> Flexible Responsive Image

- &:hover &__photo:not(:hover) {

  ​        transform: scale(.95);

  ​    }를 사용해서 hover되지 않은 컴포넌트에 css를 적용할 수 있음

- &>*을 통해서 바로 자식 emelment 선택 가능

- & *을 사용할 경우 모든 자식들 선택 가능

- 튀어나오는듯한 3D효과를 주고 싶을 경우 perspective: 위치값 을 설정해주어야함

- border-radius한 후 이미지를 넣을 때 overflow를 hidden으로 설정해주어야 제대로 적용됨

- image 두개를 섞을 때 background-blend-mode를 사용하면 쉽게 할 수 있음

  - 단, IE와 Microsoft에서는 사용 불가, Safari, Firefox, and Google Chrome은 가느

- box-decoration-break을 사용해서 줄바꿈된 문자열에 css적용방식을 정할 수 있음(clone: 독립, slice: 통합(default))

- shape-outside를 사용하여 text 정렬의 기준을 맞출 수 있음(이미지의 외관을 변경시킴)

- transform은 여러번 선언될 수 없음 -> 하위 요소에 선언되어 있으면 상속이 되지 않음

- filter속성을 사용하면 사진에 다양한 필터를 넣을 수 있음

```scss
linear-gradient(105deg, rgba($color-white, .9) 0%, rgba($color-white, .9) 50%, transparent 50%)
```

- 를 통해서 clip-path 와 동일한 효과를 사용할 수 있음
- focus양식에 맞지 않을때 설정은 focus:invalid를 통해서 할 수 있음
- +: 같은 수준에 있는 형제 요소를 선택할때사용(이후에 있어야함)
- display: table-cell을 통해서 내부를 같은 높이로 설정하는것이 간단해짐. 이때 부모는 display:table로 설정해야함
- 긴text를 자르고 싶으면 cloumn속성을 사용하면 됨
  - -count는 개수를 설정
  - -gap은 간격을 설정
  - -rule은 구분선을 설정
- visibility와 opacity를 통해 보이지 않게 설정 한 후 :target을 사용해서 #를통해 popup효과를 낼 수 있음



