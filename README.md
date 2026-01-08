- 전자책 웹뷰어(PDF/COMIC/EPUB) 기능 개발 및 성능 최적화  
- 2만 줄 규모 레거시 리팩토링(core/loader/engine 구조화) 경험  
- 관리자 CMS 페이지 개발 및 운영  
- API 기반 UI 개발 및 서비스 기능 고도화  
- Node.js 기반 서버 운영(PM2, Linux), Gulp 기반 빌드 환경 경험


### Frontend
- JavaScript(ES6+) | TypeScript / jQuery
- React, Next.js  
- Zustand, React Query  
- HTML5, CSS3, Sass  

### Backend / Infra
- Node.js, Express  
- PM2, Linux 환경 운영  
- Gulp 빌드 환경  
- REST API 연동


포트폴리오 
 - https://www.notion.so/19940711-2238d438af7180959133dc45764c17a7


src/
├─ api/
│  ├─ _api_module.ts        # api instance
│  ├─ api.comment.ts       # comment 관련 api
│  └─ api.todo.ts          # 할일 목록 관련 api
│
├─ components/
│  └─ Index/               # index 페이지 관련 component
│
│     ├─ TodoItemCommentBox/        # 할일 코멘트 박스 component
│     │  ├─ CommentList/            # 코멘트 리스트
│     │  │  ├─ CommentInputBox.tsx  # 코멘트 등록 input
│     │  │  ├─ CommentItem.tsx      # 코멘트 item
│     │  │  ├─ EmptyItem.tsx        # 코멘트가 없을 시
│     │  │  └─ index.tsx            # CommentList export
│     │  ├─ Head/                   # 할일 코멘트 박스 상단 component
│     │  ├─ BtnToggleComment.tsx    # 코멘트 등록 토글 버튼
│     │  ├─ CommentTotal.tsx        # 코멘트 전체 갯수
│     │  └─ index.tsx               # TodoItemCommentBox export
│     │
│     ├─ TodoListBox/               # 할일 목록 박스 component
│     │  ├─ Head/                   # 할일 목록 박스 상단 component
│     │  │  ├─ BtnTodoAdd.tsx       # 할일 등록
│     │  │  ├─ TotalItems.tsx       # 할일 전체 수
│     │  │  └─ index.tsx            # Head export
│     │  ├─ TodoList/               # 할일 목록 component
│     │  │  ├─ TodoItem.tsx         # 할일 item
│     │  │  └─ index.tsx            # TodoList export
│     │  └─ index.tsx               # TodoListBox export
│     │
│     ├─ TodoModal/                 # 할일 등록/수정/상세 모달 component
│     │  ├─ AddTodoModal.tsx        # 할일 등록 모달 팝업
│     │  ├─ DetailTodoModal.tsx     # 할일 상세보기 모달 팝업
│     │  ├─ TodoModal.tsx           # 공통 할일 모달 팝업
│     │  ├─ UpdateTodoModal.tsx     # 할일 수정 모달 팝업
│     │  └─ index.tsx               # TodoModal export
│     │
│     └─ shared/                    # 공용 컴포넌트
│        ├─ LayoutWrapper/          # Wrapper component
│        │  ├─ Header.tsx           # header
│        │  ├─ QueryProvider.tsx    # react-query provider
│        │  ├─ SideMenu.tsx         # side menu
│        │  └─ index.tsx            # LayoutWrapper export
│        └─ Portal.tsx              # portal component
│
├─ hook/
│  ├─ useInterSectionObserver.tsx   # 스크롤 감지 커스텀 훅
│  └─ useMutation.tsx               # useMutation 커스텀 훅
│
├─ img/                             # 컴포넌트에서 사용하는 이미지
│
├─ model/
│  ├─ comment.ts                    # comment 관련 zod schema
│  └─ todo.ts                       # 할일 관련 zod schema
│
├─ store/
│  ├─ useTodoItemCommentStore.tsx   # comment 박스 관련 zustand store
│  └─ useTodoListStore.tsx          # 할일 목록 관련 zustand store
│
├─ utils/
│  ├─ combineZero.ts                # 숫자가 10 이하일 시 앞에 0
│  ├─ createId.ts                   # json-server 랜덤 id 생성
│  └─ dateFormat.ts                 # getTime → yyyy.mm.dd hh:mm:ss
│
├─ views/
│  ├─ Error.tsx                     # 에러 페이지
│  └─ Index.tsx                     # 인덱스 페이지
│
└─ types.d.ts                       # 전역 type 정의
