# FestiGuard - 대학 축제 및 공연 큐레이션 플랫폼

FestiGuard은 대학 축제와 공연 정보를 큐레이션하고 사용자에게 맞춤형 추천을 제공하는 종합 문화 플랫폼입니다.

## 주요 기능

- **대학 축제 정보**: 전국 주요 대학 축제 일정, 장소, 출연진 정보 제공
- **공연 정보 큐레이션**: 다양한 장르의 연극, 뮤지컬 정보 제공
- **지도 기반 검색**: 서울 지역별 공연장 위치 표시 및 검색
- **장르별 필터링**: 코미디, 뮤지컬, 드라마 등 장르별 공연 검색
- **이벤트 캘린더**: 날짜별 공연 일정 확인
- **사용자 인증**: 로그인/회원가입 기능
- **커뮤니티**: 공연 리뷰, 여행 파트너 찾기, 할인 티켓 정보
- **AI 번역**: 다국어 지원 기능
- **개인화 테스트**: 사용자 취향 분석을 통한 맞춤 추천
- **바이오데이터**: 사용자 프로필 관리

## 기술 스택

- **Frontend**: React 19.1.1, React Router DOM 7.7.1
- **지도**: Kakao Maps API
- **HTTP 클라이언트**: Axios 1.11.0
- **스타일링**: CSS3
- **데이터 시각화**: TopoJSON Client 3.1.0
- **테스팅**: React Testing Library 16.3.0, Jest DOM 6.6.4
- **개발 도구**: React Scripts 5.0.1

## 프로젝트 구조

```
src/
├── components/              # 공통 컴포넌트
│   ├── Topnav.jsx          # 상단 네비게이션
│   ├── SearchModal.jsx     # 검색 모달
│   ├── SearchResults.jsx   # 검색 결과
│   ├── Review.jsx          # 리뷰 컴포넌트
│   ├── EventDetail.jsx     # 이벤트 상세
│   ├── MyTest.jsx          # 개인화 테스트
│   ├── TestResults.jsx     # 테스트 결과
│   ├── TestDatabase.jsx    # 테스트 데이터베이스
│   ├── AITranslation.jsx   # AI 번역
│   ├── DeviceInput.jsx     # 디바이스 입력
│   └── LanguageModal.jsx   # 언어 모달
├── MainPage/               # 메인 페이지
│   ├── Main.jsx            # 메인 컴포넌트
│   ├── EventCalendar.jsx   # 이벤트 캘린더
│   └── EventPanel.jsx      # 이벤트 패널
├── Map/                    # 지도 페이지
│   ├── Map.js              # Kakao Maps 연동
│   └── Map.css             # 지도 스타일
├── Genre/                  # 장르별 페이지
│   ├── Genre.jsx           # 장르 메인
│   ├── Recommended.jsx     # 추천 공연
│   └── AllPosters.jsx      # 전체 포스터
├── Community/              # 커뮤니티 기능
│   ├── Community.jsx       # 커뮤니티 메인
│   ├── CountryBoard.jsx    # 지역 게시판
│   ├── TravelPartner.jsx   # 여행 파트너
│   ├── ReviewRecommend.jsx # 리뷰 추천
│   ├── DiscountTicket.jsx  # 할인 티켓
│   └── PaymentPage.jsx     # 결제 페이지
├── Login/                  # 로그인/회원가입
│   ├── Login.jsx           # 로그인
│   └── Signup.jsx          # 회원가입
├── UserPage/               # 사용자 페이지
│   └── userPage.jsx        # 사용자 선택
├── BioData/                # 바이오데이터
│   └── BioData.jsx         # 사용자 프로필
├── ContentDetail/          # 콘텐츠 상세
│   └── ContentDetail.jsx   # 공연 상세 정보
├── FestivalDetail/         # 축제 상세
│   └── FestivalDetail.jsx  # 축제 상세 정보
├── services/               # API 서비스
│   ├── api.js              # API 클라이언트
│   ├── http.js             # HTTP 유틸리티
│   └── search.js           # 검색 서비스
├── data/                   # 데이터
│   └── festivals.js        # 축제 데이터
└── assets/                 # 정적 자산
    └── fonts/              # 폰트 파일
```

## 라우팅 구조

```
/                           # 메인 페이지
/user-selection             # 사용자 선택 페이지
/map                        # 지도 페이지
/genre                      # 장르별 페이지
/genre/recommended          # 추천 공연
/genre/all                  # 전체 포스터
/biodata                    # 바이오데이터
/community                  # 커뮤니티 메인
/community/country-board    # 지역 게시판
/community/travel-partner   # 여행 파트너
/community/review-recommend # 리뷰 추천
/community/discount-ticket  # 할인 티켓
/community/payment          # 결제 페이지
/login                      # 로그인
/signup                     # 회원가입
/search                     # 검색 결과
/content/:id                # 공연 상세 정보
/festival/:id               # 축제 상세 정보
/test/my-test               # 개인화 테스트
/test/results               # 테스트 결과
/test/database              # 테스트 데이터베이스
/ai-translation             # AI 번역
/review                     # 리뷰 작성
/event/:id                  # 이벤트 상세
```

## 시작하기

### 1. 환경 변수 설정
프로젝트 루트에 `.env` 파일을 생성하고 다음 내용을 추가하세요:

```bash
# API 기본 URL 설정
REACT_APP_API_BASE_URL=https://re-local.onrender.com/api

# 개발 환경 설정
NODE_ENV=development
```

### 2. 의존성 설치
```bash
npm install
```

### 3. 개발 서버 실행
```bash
npm start
```

### 4. 빌드
```bash
npm run build
```

## API 엔드포인트

### 기본 설정
- **Base URL**: `https://re-local.onrender.com/api`
- **Timeout**: 10초
- **Content-Type**: `application/json`

### 연극 정보 API
- **연극 목록 조회**: `GET /api/play`
  - 메인페이지 포스터용 연극 정보 조회
  - 응답: 배열 형태의 연극 데이터
- **카테고리별 조회**: `GET /api/play` (쿼리스트링으로 필터링)
  - 현재는 전체 데이터 반환 (향후 카테고리 필터링 구현 예정)

### 인증
- **토큰 기반 인증**: `Authorization: Bearer {token}`
- **자동 토큰 주입**: localStorage에서 토큰 자동 읽기
- **에러 처리**: 네트워크 에러 및 API 응답 에러 처리

## 지도 기능

- **Kakao Maps API** 사용
- 서울 지역별 공연장 위치 표시
- 지역 클릭 시 상세 정보 제공
- 주소 기반 지오코딩 지원
- TopoJSON을 이용한 서울 지역 데이터 시각화

## 주요 페이지

### 메인 페이지 (`/`)
- 추천 공연 슬라이드
- 검색 기능
- 장르별 필터링
- 이벤트 캘린더

### 지도 페이지 (`/map`)
- 공연장 위치 지도 표시
- 지역별 공연 정보

### 장르 페이지 (`/genre`)
- 장르별 공연 목록
- 추천 공연 (`/genre/recommended`)
- 전체 포스터 보기 (`/genre/all`)

### 커뮤니티 (`/community`)
- 리뷰 및 추천 (`/community/review-recommend`)
- 여행 파트너 찾기 (`/community/travel-partner`)
- 할인 티켓 정보 (`/community/discount-ticket`)
- 지역 게시판 (`/community/country-board`)
- 결제 페이지 (`/community/payment`)

### 사용자 관련
- 로그인 (`/login`)
- 회원가입 (`/signup`)
- 사용자 선택 (`/user-selection`)
- 바이오데이터 (`/biodata`)

### 테스트 및 기타
- 개인화 테스트 (`/test/my-test`)
- 테스트 결과 (`/test/results`)
- AI 번역 (`/ai-translation`)

## 대학 축제 데이터

프로젝트에는 전국 주요 대학의 축제 정보가 포함되어 있습니다:

- 건국대학교, 경희대학교, 고려대학교
- 동국대학교, 세종대학교, 서울대학교
- 서울시립대학교, 성균관대학교, 숙명여자대학교
- 중앙대학교, 한국외국어대학교, 한양대학교
- 홍익대학교, 연세대학교, 국민대학교
- 서강대학교, 한국예술종합학교

각 축제 정보에는 일정, 장소, 출연진, 포스터 이미지가 포함되어 있습니다.

## 개발 환경

- Node.js 16+
- React 19.1.1
- npm 또는 yarn
- React Scripts 5.0.1

## 라이선스

이 프로젝트는 MIT 라이선스 하에 있습니다.