# codestates-fe-advanced-course



# 완성된 GIF 파일 및 배포링크
https://ace0507.github.io/codestates-fe-advanced-course/
![board](https://user-images.githubusercontent.com/82556064/183034476-b1b72e49-eb2f-4ac8-ac19-580fad27f508.gif)




# 프로젝트 실행 방법
cd client → npm install → npm start

 
# 사용한 스택 목록
- JavaScript
- React
- HTML
- Styled-component


# 구현한 기능 목록 (Software Requirement Specification)
- 게시물 리스트
- 게시물 상세 페이지
- 댓글
- 페이지네이션
- 모달창


# 구현 방법 혹은 구현하면서 어려웠던 점
- 마지막에 배포가 되지 않아서 어려움을 겪었다. basename={process.env.PUBLIC_URL}을 <Router> 태그에 넣었어야하는데 <Routes>에 넣었기 때문인데 이런 잔실수를 줄어야겠다고 생각했다.
- 댓글을 불러오는 과정에서 처음엔 useState의 초기 상태를 빈객체로 두었더니 아무 댓글도 들어오지 않아서 뭐가 문제인지 잘 몰랐다. 객체에 name: "", body: ""를 추가하자 들어왔다.


# Prototype
https://www.figma.com/file/sqHCLIHFxWNiVYF2tTwaIj/Untitled?node-id=0%3A1


# 성능 최적화에 대해서 고민하고 개선한 방법
- 페이지네이션 에서 사용시 매번 데이터를 불러오게 되면 실행 속도 및 과도한 트래픽이 발생 할 수 있다. 그래서 화면 생성 초기 1번만 호출하여 랜더링한 후 display: none을 사용하여 처리하여다.
- a태그 대신 Link 태그를 사용하여 브라우저의 주소만 바꿀 뿐 다시 렌더링 하지 않아서 빠르고 부드러운 화면 전환이 가능하다.


# 추가 구현 사항에 대한 구현 방법과 설명
- 페이지네이션: 1~10번 까지의 번호와 앞,뒤 아이콘을 합쳐 총 12개의 버튼을 map으로 돌렸고, 해당 index가 들어오면 그에 해당하는 페이지를 보여주었다.  
- 모달창: useState를 사용하여 초기에는 "none"으로 설정해두고 onClick이 일어나면 setModalDisplay로 "block"으로 보여주었다. (이 곳에서는 정렬을 위해 block대신 "flex"사용) 



