# JBSW NOW

## AI 기반 전북권 대학 및 SW 사업단 통합 정보 플랫폼

![스크린샷 2025-12-25 오전 4 47 18](https://github.com/user-attachments/assets/d559a619-a3c8-44be-93ac-6e4c1fc06a88)


---

## 프로젝트 소개

전북권 내 대학(전북대, 군산대, 원광대) 및 SW 관련 사업단에서 주최하는 다양한 행사와 이벤트 정보를 통합하여 제공하는 정보 플랫폼입니다.

각 기관별 웹사이트의 주요 게시판 콘텐츠를 주기적으로 수집(크롤링)하여 보여줍니다. 이를 통해 사용자에게는 핵심 요약, 태그별 정보 추천, 실시간 푸시 알림, RAG 기반 챗봇 등의 경험을 제공합니다.

기존의 흩어져 있던 정보를 찾기 위해 사용자가 각 사이트를 방문하여 정보를 직접 수집했던 불편함을 해소합니다.

- **`@M-SE0K`** - 풀스택 개발 담당
- **`@cheoleon`** - 백엔드 개발 담당
- **`@do-ttery`** - UI/UX 기획 및 디자인, 프론트엔드 개발
- **`@igaeun8`** - UI/UX 기획 및 디자인

---

## 배포 주소

**웹 버전**: [http://113.198.66.75:18016](http://113.198.66.75:18016/auth/login?redirect=%2F)

---

## 주요 기능

- **홈 화면** - 최신 소식, 인기 이벤트, 빠른 메뉴 접근
- **소식 페이지** - 전북권 대학 및 SW 사업단 공지사항 및 이벤트 통합 제공
- **저장 페이지** - 즐겨찾기한 콘텐츠 모아보기
- **인기 페이지** - 조회수 및 관심도 기반 인기 콘텐츠 추천
- **AI 챗봇** - RAG 기반 지능형 챗봇을 통한 정보 검색 및 요약
- **검색** - 전체 콘텐츠 통합 검색 및 태그별 필터링
- **알림** - 관심 태그 및 키워드 기반 푸시 알림
- **설정** - 다크 모드, 사용자 선호도, 알림 설정 관리

> **상세 기능 설명**: 각 기능별 및 페이지별 상세 설명은 [Notion 문서](링크_추가)에서 확인할 수 있습니다.

---

## 기술 스택

<span><img src="https://img.shields.io/badge/reactnative-61DAFB?style=for-the-badge&logo=react&logoColor=black"></span>
<span><img src="https://img.shields.io/badge/node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/express-009922?style=for-the-badge&logo=express&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/Expo-000000?style=for-the-badge&logo=Expo&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white"></span>

### Frontend
- **React Native** - 크로스 플랫폼 모바일 앱 개발
- **Expo** - React Native 개발 환경 및 배포
- **TypeScript** - 타입 안정성 보장
- **Expo Router** - 파일 기반 라우팅
- **React Query** - 서버 상태 관리

### Backend
- **Node.js** - 서버 런타임
- **Express** - 웹 프레임워크
- **Firebase** - 백엔드 서비스 (Firestore, Authentication)
- **Google Gemini API** - AI 기반 콘텐츠 분석 및 챗봇
- **Ollama** - 로컬 LLM 지원 (선택적)

---

## 프로젝트 구조

```
JBSW-NOW/
├── app/                   # Expo Router 페이지
│   ├── auth/              # 인증 페이지 (로그인, 회원가입)
│   ├── chat/              # AI 챗봇 페이지
│   ├── events/            # 소식/이벤트 페이지
│   ├── favorites/         # 저장 페이지
│   ├── hot/               # 인기 페이지
│   ├── search/            # 검색 페이지
│   ├── notification/      # 알림 페이지
│   └── settings/          # 설정 페이지
├── src/
│   ├── api/               # API 클라이언트
│   ├── components/        # 재사용 가능한 컴포넌트
│   ├── services/          # 비즈니스 로직
│   ├── types/             # TypeScript 타입 정의
│   └── utils/             # 유틸리티 함수
├── server/                # Express 서버
├── scripts/                # 유틸리티 스크립트
└── data/                  # 테스트 데이터
```

---

## 개발 환경 구축 및 실행

### 필수 요구사항

- Node.js 18 이상
- npm 또는 pnpm
- Expo CLI

### 프로젝트 클론

```bash
git clone https://github.com/M-SE0K/JBSW-NOW.git
cd JBSW-NOW
```

### 설치 및 세팅

자동 설치 스크립트를 실행하여 모든 의존성을 설치합니다:

```bash
npm run setup
```

또는 수동 설치:

```bash
# 프로젝트 의존성 설치 (react-native-svg 포함)
npm install

# 또는 react-native-svg만 별도 설치하는 경우
npm install react-native-svg
```

### 실행 방법

#### Expo 개발 서버 실행

```bash
# 캐시 클리어 후 개발 서버 시작
npx expo start -c
```

#### 백엔드 서버 실행 (선택사항)

Ollama 서버가 필요한 경우:

```bash
# 서버 컴퓨터 SSH 접속 및 모델 실행
OLLAMA_HOST=123.123.123.123 ollama serve
```

프록시 서버 실행:

```bash
# Ollama URL 지정하여 프록시 실행
OLLAMA_URL=IP:포트번호 npm run proxy

# 간단한 프론트 확인을 위한 프록시 실행
npm run proxy
```
