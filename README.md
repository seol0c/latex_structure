<pre> 노트북에서 테스트
book/
├── principles of physics/   일반물리 교재를 만드는 경우
│   ├── appendix/            부록 - 넘버링, 양식이 다르기 때문에 따로 별도 체계 위해 분리
│   │  ├── appendix01.tex    실험 방법 요약
│   │  ├── appendix02.tex    추가 그래프 모음
│   │  ├── appendix03.tex    설문지 원본, 코드 목록 등을 분리해서 사용
│   │  └── ...
│   │
│   ├── bib/                 참고문헌 - 아무렇게나 써도 추후 정렬(참조순, 가나다순 등)할 수 있음
│   │  ├── references.bib     메인 참고문헌 (책, 논문 등 전통적 자료)
│   │  ├── websites.bib       웹사이트 출처 (블로그, 통계청, 공식 발표 등)
│   │  └── papers.bib         학술 논문만 따로 구분
│   │
│   ├── chapters/              본문 내용
│   │   ├── 00/
│   │   ├── 14/
│   │   ├── 18/                18장 폴더
│   │   │   ├── figures/       그림 파일 모음
│   │   │   ├── chapter.tex    chapter - 모든 section, table, figure 호출
│   │   │   ├── section01.tex
│   │   │   ├── section02.tex
│   │   │   ├── section03.tex
│   │   │   ├── section04.tex
│   │   │   ├── section05.tex
│   │   │   ├── section06.tex
│   │   │   └── tables.tex
│   │   ├── 19/
│   │   └── 20/
│   │
│   ├── includes/
│   │   ├── preface.tex        서문
│   │   ├── title.tex          제목, 저자 등 표지글
│   │   └── toc.tex            목차
│   │
│   ├── main/                  메인 조립 디렉토리
│   │   ├── main.tex           메인 컴파일 파일
│   │   ├── main.pdf           최종 산출 PDF
│   │   └── ...                기타 보조 파일(.aux, .log 등)
│
├── structure/                 사용자 정의 매크로(\newcommand) 저장 - 반복 스타일(색, 강조) 통합
│   ├── box.sty                박스, 테두리 등 시각적 요소
│   ├── format.sty             문단, 서식 전반 포맷 정의
│   ├── package.sty            패키지 로드 및 기본 옵션
│   ├── page.sty               페이지 레이아웃 및 번호 스타일
│   ├── preamble.tex           *main에서 preamble만 호출
│   ├── seolf.sty              seolmode 관련 함수 정의
│   ├── tablefigure.sty        표와 그림 관련 함수 정의
│   └── README.md              구조 및 규칙 설명

모든 경로 해석은 main.tex 기준이므로, structure의 파일에 가려면 두 단계 상위 계열로 올라가야 함.
예를 들어 다음과 같이 사용함.
\input{../../structure/preamble.tex}
</pre>