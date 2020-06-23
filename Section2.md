1. *을 사용해서 원하지 않은 기본 margin과 padding을 없애고 box-sizing과 같은 모든 div에 적용되길 원하는 설정값을 명시하라
2. body를 통해서 div들에 상속되길 원하는 값들을 명시하라 (상속되지 않는 속성들도 존재)
3. %를 사용하기 보다는 vh를 사용하라
4. 그라데이션 효과를 사용하는 방법: linear-gradient(to , 색상...)
5. background-image는 여러개 쌓을 수 있다.
6. clip-path를 사용해서 div를 자를 수 있다.[폴리곤 쉽게 사용하기](https://bennettfeely.com/clippy/)
   1. polygon()을 사용하자
7. background-position 속성을 사용하면 이미지가 화면에서 전부 드러나지 않을 때 어느부분을 중심으로 할것인지 설정 가능



 	1. img의 alt는 검색을 위해서 사용되고 추가적으로 이미지가 표시되지 않을때도 사용된다.
 	2. absolute는 position: static 속성을 가지고 있지 않은 부모를 기준으로 움직임(만약 없다면 body가 기준)
 	3. google 검색엔진에서 h1의 값을 웹페이 내용 파악에 중요하게 다룸
 	4. position을 사용해서 top left를 조절하면 부모와 관련되어 변경되고 transform을 사용하면 자신의 길이 높이를 사용해서 조절할 수 있음(이를 통해서 가운데 배치가 가능해짐)



1. keyframes를 사용하여 에니메이션을 만들 수 있음 각 %별로 표시. 
   1. 성능을 위해서 2가지 기능만 추가하는것이 좋음



1. [pseudo-class](https://developer.mozilla.org/ko/docs/Web/CSS/Pseudo-elements) 를 사용해서 일부분에만 스타일을 입힐 수 있음
   1. :link와 :visited를 한 번에사용해서 링크에 방문 전 후 스타일이 모두 동일하게 적용시킬 수 있음
2. transition: all을 사용할 때 background가 설정되어 있으면 처음 시작할 때 가운데부터 이미지가 생성되는것처럼 연출된다.



1. ::after을 통해서 div를 생성할 수 있다.
   1. 이때 생성된 div는 자식element로 들어가게 된다. 따라서 height, width의 비율은 after가 붙은 element의 비율에 맞춰진다.
2. animation-fill-mode를 통해서 element의 초기 상태를 animation이 시작되기 전/후의 상태로 설정할 수 있다.

