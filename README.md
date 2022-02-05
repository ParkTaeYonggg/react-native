# react-native

### 초기세팅
[참고](https://reactnative.dev/docs/environment-setup)
!! cli을 쓰는 이유는 커스텀이 용이하기 때문이라고 알고 있다. (2022-02-05)

-  위 참고를 보고 세팅이 끝났으면 홈디렉토리로 돌아가서 
   npm i -g react-native를 설치해준다.
-  npx react-native init 사용할 리액트네이티브 폴더명 --template react-native-template-typescript 를 설치해준다.
그리고 실행해준다.

### 이건 모르면 안 된다.
- 환경변수가 일치해야 한다. (adb, node 등등) : 이걸 확인하려면 "which --찾을파일"을 입력해주자.
- 처음 만들어진 리액트네이티브 파일 역할
  1. app.json : 앱의 이름을 결정해주는 곳
      ->이거 처음부터 잘 설정하고 들어가야 함. 안그러면 변경해야 할 점들이 많음 (ios, android, index.js 등등 다 변경 해야함)
  3. tsconfig, index.js, app.tsx, pacakge.json(+lock), babel.config.js 은 리액트와 같음
  4. app폴더 : 이건 60 쯤인가 이전에 직접 설정했어야 했는데 최근 오토로 변함. -> 건들지 않을 것임.
- 리액트네이티브 내에서 스타일시트로 어떤 수치를 넣을 땐 dip 라는 수치가 되겠다. -> 기기 별 화면에 따라 자동으로 계산해서 같은 넓이 등을 적용해줌?
  (해상도에 따라 결정됨)
- safeAreaVeiw : 이건 노치 부분을 자동으로 피해갈 수 있도록 만들어 준다. 그리고 하단에 화면 가리는 부분도 피할 수 있따.
- scrollView : 단점은 성능의 문제가 발생하지만 (대응책은 flatList), 많은 컨텐츠들을 담을 때 사용한다. -> 스크롤 이벤트가 크기에 따라 자동으로 생성되나 보다.
- style 적용 : 스타일시트로 대부분 만들지만 조건문 등을 적용할 때에는 태그에 직접 스타일 배열을 통해 넣어준다. ex) <View style = \{\[객체, \{color: 들어갈 내용}\]\} 
- watchman : 리액트 네이티브의 변화가 일어 났을 때 그 변화를 감지하고 자동으로 빌드시켜 

