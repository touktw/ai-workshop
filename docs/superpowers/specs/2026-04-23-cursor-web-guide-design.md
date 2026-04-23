# Design Spec: Cursor로 시작하는 웹 개발 입문 가이드

Date: 2026-04-23

## 개요

개발 지식이 전혀 없는 비개발자(기본 컴퓨터 활용 능력 보유)를 대상으로,
Cursor AI 에디터를 활용해 맥북 환경 세팅부터 할 일 목록 웹앱 완성까지
단계별로 안내하는 한국어 가이드 문서 모음.

## 대상 독자

- 맥북 사용자
- 코딩 경험 없음, 파일/인터넷 활용 가능한 수준
- 예상 소요 시간: 2~3시간

## 파일 구조

```
ai-workshop/
├── README.md
├── 01-cursor-setup.md
├── 02-mac-setup.md
├── 03-first-project.md
├── 04-build-todo.md
├── 05-run-and-test.md
└── images/
    └── (스크린샷 placeholder 파일들)
```

## README.md 구성

- Summary: 가이드 목적 및 대상 한 단락 소개
- TOC: 각 챕터 파일 링크 포함 번호 목록
- 준비물: 맥북, 인터넷, 예상 시간

## 각 챕터 내용

| 파일 | 주요 내용 |
|------|-----------|
| `01-cursor-setup.md` | Cursor 홈페이지 가입 → 다운로드 → 설치 → 첫 실행 확인 |
| `02-mac-setup.md` | 터미널 여는 법 → Homebrew 설치 → Node.js/npm 설치 → 버전 확인 |
| `03-first-project.md` | 프로젝트 폴더 생성 → Cursor에서 폴더 열기 → 파일 구조 소개 |
| `04-build-todo.md` | Cursor AI로 할 일 목록 앱 생성 요청 → 코드 설명 → 수정해보기 |
| `05-run-and-test.md` | 브라우저로 index.html 열기 → Live Server 설치 → 동작 확인 |

## 포맷 규칙

- 언어: 한국어 (기술 용어는 영어 유지)
- 모든 명령어: 코드블록 사용 필수 (copy/paste 용이)
- 팁/주의사항: `> 💡` 또는 `> ⚠️` 박스 사용
- 스크린샷: `![설명](images/xx-yyy.png)` placeholder 삽입
- 각 챕터 상단: "이 챕터에서 할 것" 한 줄 요약
