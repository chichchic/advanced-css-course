

###1

- SASS는 CSS에서 제공하지 않은 몇가지 편리한 기능들을 통해 CSS를 만들어 내는 CSS preprocessor이다.
  (SASS를 Compile하면 CSS가 나온다.)
- 특징
  - Variables
  - Nesting
  - Operators
  - Partials and imports
  - Mixins
  - Functions
  - Extends
  - Control directives

- 두가지 syntax가 있음(들여쓰기, 괄호사용)

### 3

- nesting

  - 내부에 적어주는것만으로도 속성내부에 속성을 설정할 수 있음

    .navigation{

    ​	//.navigation li

    ​	li{

    ​	}

    }

  - 공백을 원하지 않을 경우 &을 앞에 붙여서 사용하면 됨

  - display: table -> 자식 요소의 수별로 공간을나누어 보여줌

  - clear: both -> float에서 좌우에 줄바꿈

  - darken(변수, 비율%), lighten(변수, 비율%) -> 색상의 밝기 조절

### 4

- Mixin
  - @mixin 이름 으로 정의하고 @include 이름으로 사용
    - argument를 사용해서 함수처럼 사용할수 있음
- Extend
  - %이름 으로 정의하고 @extend 이름 으로 사용
    - mixin은 내부에 속성이 들어오는 방식으로 compile된다면 extend는 외부에 속성이 생성되는 방식으로 사용된다
  - 서로 관련있는 상황에서만 사용해야 효율적임

### 5

- node-sass를 통해서 npm을 사용한 compile이 가능함
- npm에서 -w option을 추가하면 지속적으로 변화를 지켜보도록 만들 수 있음
- live-server를 통해서 html창에 변화를 자동으로 인식하게 할 수 있음



