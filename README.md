# Movie App 2020

React JS Fundamental Coures (2019 Update!)

- npx create-react-app name  
  google drive file stream에서 실행하다가  
  에러발생 : npm err maximum call stack size exceeded  
  c드라이브 documents에서 하니까 된다.

- github에 넣기  
  github에서 똑같은 이름 Repository 만들기  
  git init  
  git add .  
  git commit -m "수정한 내용"  
  git branch -M main  
  git remote origin 내URL  
  git push -u origin main  
  github는 기본 브랜치를 master에서 main으로 변경 2020.10.01. 부터

- README.md 작성법

  - 줄 바꿈 : 글 끝에서 space 2번
  - 문단 바꿈 : enter 2번

- public폴더  
  favicon.ico : 탭에 나오는 그림

- react  
   react는 소스코드에 처음부터 HTML을 넣지 않고,  
   HTML을 추가하거나 제거하는 법을 안다.  
   component에 작성한 것을 HTML에 밀어넣는다.  
   component : HTML을 반환하는 함수  
   component 작성할 때마다 import React from 'react'; 해야함 아니면 jsx가 이해하지 못함  
   jsx : js와 HTML 사이의 조합,  
   component를 만들고 어떻게 사용하는지에 대한 것?  
   react는 한 번에 하나의 component만을 rendering할 수 있다  
   그래서 App.js 안에 component들을 다 넣어야한다(import).  
   component는 재사용 가능  
  component는 대문자로 시작해야한다.  
  ex) <Food fav="kimchi" />  
  Food : component, fav : props  
  npm i prop-types : prop다르면 찾아줌

- state  
  function component는 function이고 뭔가를 return하고  
  class component는 class야 하지만 react component로 부터 확장되서  
  render 메소드 안에 넣어야 한다.  
  그러면 react는 자동적으로 class component의  
  render method를 실행한다.  
  state는 object이고 component의 data를 넣을 공간이 있고  
  이 **데이터는 변한다**. state사용하는 이유  
  class component안에 state를 사용하려면  
  {this.state.데이터}  
  setState를 호출하면 react는 state를 refresh하고  
  render를 실행한다.

- component life cycle
  mounting: 태어나는 것  
  updating: 일반적인 업데이트  
  unmounting: component가 죽는 것(페이지 바꿀 때)

  - 함수 실행 순서  
    component -> render -> componentDidMount
  - setState 호출시 실행 순서  
    component -> render -> componentDidUpdate

- axios  
  axios는 fetch 위에 있는 작은 layer  
  예를 들면 axios는 땅콩 주위의 멋진 초콜릿???  
  npm install axios  
  yts 영화 api 사용
  axios로 부터 온 data를 잡아야한다  
  그래야 state를 사용할 수 있다  
  axios는 빠르지 않아서 componentDidMount 함수가 끝날  
  때까지 시간이 걸릴 수 있다고 말해주고 기다린다. async, await

- es6는 ECMA script  
  movies.data.data.movies 를
  const { data: { data: { movies }}} 로 바꿀 수 있다

- rendering movies  
  map을 사용하면 map으로부터 뭔가를 return해야함

- javascript class 안에 있으면  
  component class에 의해 react가 혼란스러워 한다  
  안에 html의 속성 class -> className 으로 바꾼다.

- map function은 여러 argument를 준다.  
  item과 item number(index, number)를 보여준다.

- Deploying to github pages

  1. gh-pages설치 만든 웹사이트를 github page에 나타낸다. 새 터미널을 연다.  
     npm i gh-pages
  2. github에서 project이름(movie_app)을 가져온다.  
     git remote -v
  3. package.json에서 home page 추가  
      프로젝트 이름은 무조건 소문자고, 공백 허용 안함  
     "homepage": "https://gunwoo8622.github.io/movie_app"
  4. 원래있던 터미널에서 react서버를 내리고  
     npm run build  
     작업들을 최소화한 build폴더가 만들어진다.  
     build폴더를 gh-pages에 업로드 한다.  
     package.json에서 scripts 안에 deploy를 추가
     "deploy": "gh-pages -d build"  
     deploy를 호출하면 먼저 predeploy가 호출된다  
     폴더이름(build)이 같아야 실행된다.  
     "predeploy": "npm run build"

- react hook(새로운 것)  
  state를 갖기 위해 class component를 가질 필요가 없다.

- react-router-dom  
  네비게이션 만들어주는 패키지  
  npm install react-router-dom

- route란

- a href 쓰면 강제로 새로고침되면서 react죽인다?  
  Link to 를 쓴다. router안에서만 작동된다.  
  router안에 모든 걸 넣을 필요는 없다.

- HashRouter #이 붙어있음  
  BrowserRouter #이 없지만 git pages에 정확히 설정하기 힘들다.

- route props  
  라우터에 있는 모든 라우터들은 props를 가진다.  
  props를 사용할 줄 알아야한다. 정보를 전달하기 위해  
  링크를 통해 정보를 라우터로 보낸다.(movie.js)

-
