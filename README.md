# JBSW NOW

**AI 기반 전북권 대학 및 SW 사업단 통합 정보 플랫폼**
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0454dbfd-2905-443b-856d-4c0db8f02c76" />

전북권 내 대학(전북대, 군산대, 원광대) 및 SW 관련 사업단에서 주최하는 다양한 행사와 이벤트 정보를 통합하여 제공하는 정보 플랫폼입니다.
각 기관별 웹사이트의 주요 게시판 콘텐츠를 주기적으로 수집(크롤링)하여 보여줍니다. 
이를 통해 사용자에게는 핵심 요약, 태그별 정보 추천, 실시간 푸시 알림, RAG 기반 챗봇 등의 경험을 제공합니다.

## 주요 기능

### 홈 화면
- 최신 소식 및 이벤트 실시간 표시
- 인기 이벤트 배너 슬라이더
- 빠른 메뉴 접근 (소식, 저장, 인기, 검색 등)
- 태그 기반 콘텐츠 분류 및 추천

### 소식 페이지
- 전북권 대학 및 SW 사업단의 모든 공지사항 및 이벤트 통합 제공
- 실시간 검색 기능
- 태그별 필터링 (수강, 졸업, 학사, 취업, 공모전, 봉사활동 등)
- 상세 정보 및 원본 링크 제공

### 저장 페이지
- 즐겨찾기한 공지사항 및 이벤트 모아보기
- 오프라인에서도 저장된 항목 확인 가능

### 인기 페이지
- 조회수 및 관심도 기반 인기 콘텐츠 추천
- 실시간 인기 순위 업데이트

### AI 챗봇
- RAG(Retrieval-Augmented Generation) 기반 챗봇
- 자연어 질의를 통한 정보 검색 및 요약
- 빠른 프롬프트 제공 (오늘 공지 요약, 다가온 행사 일정 등)
- 마크다운 형식 응답 지원

### 검색
- 전체 콘텐츠 통합 검색
- 태그 및 카테고리별 검색 필터
- 실시간 검색 결과 제공

### 알림
- 관심 태그 및 키워드 기반 푸시 알림
- 실시간 공지사항 업데이트 알림

### 설정
- 다크 모드 지원
- 사용자 선호도 설정
- 알림 설정 관리

## 기술 스택
<span><img src="https://img.shields.io/badge/reactnative-61DAFB?style=for-the-badge&logo=react&logoColor=black"></span>
<span><img src="https://img.shields.io/badge/node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/express-009922?style=for-the-badge&logo=express&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/Expo-000000?style=for-the-badge&logo=Expo&logoColor=white"></span>
<span><img src="https://img.shields.io/badge/firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white"></span>



---

## 개발환경 구축 및 실행

### 프로젝트 클론

```bash
git clone https://github.com/M-SE0K/JBSW-NOW.git
cd JBSW-NOW
```

### 설치 및 세팅 `/script/stup.mjs`

```bash
npm run setup
```

### 필수 패키지 설치

```bash
# 프로젝트 의존성 설치 (react-native-svg 포함)
npm install

# 또는 react-native-svg만 별도 설치하는 경우
npm install react-native-svg
```

### 실행 방법

```bash

//expo 크로스 플랫폼 실행
npx expo start -c

//서버 컴퓨터 ssh 접속 및 모델 실행
OLLMA_HOST=123.123.123 olama server

//프록시 실행
OLLAMA_URL=IP:포트번호 npm run proxy

//간단한 프론트 확인을 위한 프록시 실행
npm run proxy


```

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
├── scripts/               # 유틸리티 스크립트
└── data/                  # 테스트 데이터
```

## 배포 주소
```
http://113.198.66.75:18016
```
