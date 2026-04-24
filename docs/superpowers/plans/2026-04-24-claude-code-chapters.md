# Claude Code 챕터 추가 (06~08) Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 5단계 가이드를 마친 입문자가 Claude Code를 Cursor와 함께 사용할 수 있도록 안내하는 챕터 3개(06~08)와 README 업데이트를 작성한다.

**Architecture:** 마크다운 파일 3개 신규 생성 + README.md 목차 업데이트. 이미지 없음, 텍스트만으로 UI 위치 안내. 기존 챕터 스타일(친근한 한국어, 기술 용어 최소화) 유지.

**Tech Stack:** Markdown, 기존 ai-workshop 가이드 구조

---

## 파일 구조

| 작업 | 파일 경로 |
|------|-----------|
| 신규 생성 | `06.Claude-Code-시작하기.md` |
| 신규 생성 | `07.터미널로-Claude-Code-사용하기.md` |
| 신규 생성 | `08.Cursor에서-Claude-Code-사용하기.md` |
| 수정 | `README.md` (목차 항목 3개 추가) |

---

## Task 1: 06.Claude-Code-시작하기.md 작성

**Files:**
- Create: `06.Claude-Code-시작하기.md`

- [ ] **Step 1: 파일 생성**

아래 내용 그대로 `06.Claude-Code-시작하기.md` 파일을 생성한다.

```markdown
# 6단계: Claude Code 시작하기

> 이 챕터에서 할 것: Claude Code가 무엇인지 알아보고, 설치 및 로그인까지 완료합니다.

---

## 6-1. Claude Code란?

Cursor AI가 에디터 창 안에서 코드를 수정해 준다면,  
**Claude Code는 터미널(명령어 창)에서 AI와 직접 대화하며 작업하는 도구**입니다.

코드를 설명하고, 기능을 추가하고, 버그를 고치는 것을 — 채팅 형식으로 요청할 수 있습니다.  
만든 회사도 Claude AI와 같은 Anthropic이라서 성능이 뛰어납니다.

---

## 6-2. claude.ai 가입하기

Claude Code를 사용하려면 먼저 Anthropic 계정이 필요합니다.

1. 브라우저에서 **claude.ai** 를 엽니다.
2. **Sign up** 버튼을 클릭합니다.
3. 이메일 주소 또는 Google 계정으로 가입합니다.
4. 이메일 인증을 완료합니다.

> 💡 이미 claude.ai 계정이 있다면 이 단계를 건너뛰세요.

---

## 6-3. Node.js 설치 확인

Claude Code를 설치하려면 Node.js가 필요합니다.  
2단계에서 이미 설치했지만, 한 번 확인해 봅시다.

터미널을 열고 아래 명령어를 입력하세요:

```bash
node --version
```

`v18.0.0` 이상의 버전이 표시되면 정상입니다.

> 💡 버전이 표시되지 않으면 [맥 개발환경 세팅하기](02.맥-개발환경-세팅.md)를 다시 확인하세요.

---

## 6-4. Claude Code 설치하기

터미널에서 아래 명령어를 입력하세요:

```bash
npm install -g @anthropic-ai/claude-code
```

설치가 완료될 때까지 잠시 기다립니다. (1~2분 소요)

설치가 완료되면 버전을 확인합니다:

```bash
claude --version
```

버전 번호가 표시되면 설치 성공입니다. 🎉

---

## 6-5. 로그인하기

아래 명령어로 로그인합니다:

```bash
claude login
```

브라우저가 자동으로 열리며 Anthropic 로그인 화면이 나타납니다.

1. 6-2에서 만든 계정으로 로그인합니다.
2. **Allow** 버튼을 클릭합니다.
3. 터미널에 `Logged in successfully` 메시지가 표시되면 완료입니다. ✅

---

## 다음 단계

이제 Claude Code를 사용할 준비가 됐습니다!

- [터미널에서 사용하기 →](07.터미널로-Claude-Code-사용하기.md)
- [Cursor 안에서 사용하기 →](08.Cursor에서-Claude-Code-사용하기.md)

---

이전 단계: [← 브라우저에서 확인하기](05.브라우저에서-확인하기.md)  
[← 목차로 돌아가기](README.md)
```

- [ ] **Step 2: 내용 검토 — 입문자 기준 확인**

아래 기준으로 파일을 직접 읽어보고 확인한다:
- 기술 용어(API, CLI 등)가 설명 없이 사용된 부분 없는지
- 각 단계가 독립적으로 이해 가능한지
- 명령어 코드블록이 정확한지 (`npm install -g @anthropic-ai/claude-code`, `claude login`)

- [ ] **Step 3: 커밋**

```bash
git add 06.Claude-Code-시작하기.md
git commit -m "docs: 06. Claude Code 시작하기 챕터 추가"
```

---

## Task 2: 07.터미널로-Claude-Code-사용하기.md 작성

**Files:**
- Create: `07.터미널로-Claude-Code-사용하기.md`

- [ ] **Step 1: 파일 생성**

아래 내용 그대로 `07.터미널로-Claude-Code-사용하기.md` 파일을 생성한다.

```markdown
# 7단계: 터미널로 Claude Code 사용하기

> 이 챕터에서 할 것: 터미널에서 Claude Code를 실행하고, 할 일 목록 앱에 새로운 기능을 추가합니다.

> ⚠️ 먼저 [6단계: Claude Code 시작하기](06.Claude-Code-시작하기.md)를 완료해야 합니다.

---

## 7-1. 터미널에서 프로젝트 폴더 열기

터미널을 열고 할 일 앱 폴더로 이동합니다.

```bash
cd ~/Desktop/my-todo-app
```

> 💡 `cd`는 "change directory"의 약자로, 폴더를 이동하는 명령어입니다.  
> 폴더 위치가 다르다면 `cd` 뒤에 실제 경로를 입력하세요.

현재 위치를 확인하려면:

```bash
pwd
```

`/Users/내이름/Desktop/my-todo-app` 같은 경로가 표시되면 정상입니다.

---

## 7-2. Claude Code 실행하기

아래 명령어로 Claude Code를 시작합니다:

```bash
claude
```

잠시 후 아래와 같은 화면이 나타납니다:

```
✻ Welcome to Claude Code!

  /help for help, /exit to exit

>
```

`>` 뒤에 원하는 것을 자유롭게 입력하면 됩니다.

---

## 7-3. 실습: 완료된 항목 수 표시하기

할 일 앱 상단에 완료된 항목 수를 표시하는 기능을 추가해 봅시다.

아래 내용을 그대로 입력하세요:

```
완료된 할 일 개수를 앱 상단에 "완료: 2개 / 전체: 5개" 형식으로 표시해줘
```

Claude Code가 코드를 분석하고 수정합니다.  
수정이 완료되면 어떤 파일을 어떻게 바꿨는지 설명해 줍니다.

---

## 7-4. 결과 확인하기

Cursor로 돌아가서 Live Server가 실행 중인지 확인합니다.  
브라우저에서 앱을 새로고침(`Command(⌘) + R`)하면 변경된 내용이 보입니다.

> 💡 Live Server가 꺼져 있다면 Cursor 하단 상태 표시줄에서 **Go Live**를 클릭하세요.

---

## 7-5. 대화 이어가기

한 번으로 끝내지 않아도 됩니다. 마음에 들지 않으면 바로 요청하면 됩니다:

```
색상을 파란색으로 바꿔줘
```

```
글씨 크기를 조금 더 크게 해줘
```

Claude Code는 이전 대화를 기억하면서 수정합니다.

---

## 7-6. 종료하기

작업이 끝났으면 아래 명령어로 종료합니다:

```
/exit
```

또는 `Ctrl + C`를 누릅니다.

---

## FAQ

**Q. `claude` 명령어가 없다고 나와요.**  
6단계에서 설치가 제대로 됐는지 확인하세요. `npm install -g @anthropic-ai/claude-code`를 다시 실행해 보세요.

**Q. 수정했는데 브라우저에서 변경이 안 보여요.**  
`Command(⌘) + R`로 브라우저를 새로고침하거나, Live Server를 재시작해 보세요.

**Q. Claude Code가 엉뚱한 걸 수정했어요.**  
더 구체적으로 요청하면 됩니다. 예: "index.html 파일에서 h1 태그 바로 아래에 추가해줘"

---

이전 단계: [← Claude Code 시작하기](06.Claude-Code-시작하기.md)  
다음 단계: [Cursor에서 Claude Code 사용하기 →](08.Cursor에서-Claude-Code-사용하기.md)  
[← 목차로 돌아가기](README.md)
```

- [ ] **Step 2: 내용 검토**

아래 기준으로 확인한다:
- `cd ~/Desktop/my-todo-app` 경로가 04단계에서 만든 앱 위치와 일치하는지
- 실습 프롬프트 예시가 자연스러운지
- FAQ가 실제로 발생할 오류를 커버하는지

- [ ] **Step 3: 커밋**

```bash
git add 07.터미널로-Claude-Code-사용하기.md
git commit -m "docs: 07. 터미널로 Claude Code 사용하기 챕터 추가"
```

---

## Task 3: 08.Cursor에서-Claude-Code-사용하기.md 작성

**Files:**
- Create: `08.Cursor에서-Claude-Code-사용하기.md`

- [ ] **Step 1: 파일 생성**

아래 내용 그대로 `08.Cursor에서-Claude-Code-사용하기.md` 파일을 생성한다.

```markdown
# 8단계: Cursor에서 Claude Code 사용하기

> 이 챕터에서 할 것: Cursor 안에 Claude Code 확장을 설치하고, 에디터에서 바로 AI와 대화하며 할 일 앱을 개선합니다.

> ⚠️ 먼저 [6단계: Claude Code 시작하기](06.Claude-Code-시작하기.md)를 완료해야 합니다.

---

## 8-1. Claude Code 확장 설치하기

1. Cursor 왼쪽 사이드바에서 블록 모양 아이콘(Extensions)을 클릭합니다. (단축키: `⇧⌘X`)
2. 검색창에 `Claude Code`를 입력합니다.
3. **Claude Code** (제작: Anthropic)를 찾아 **Install**을 클릭합니다.
4. 설치가 완료되면 Cursor를 재시작합니다.

---

## 8-2. Claude Code 패널 열기

재시작 후 두 가지 방법으로 Claude Code를 열 수 있습니다.

**방법 1. 터미널 패널 사용**
1. Cursor 상단 메뉴에서 **Terminal → New Terminal**을 클릭합니다. (단축키: `` Ctrl+` ``)
2. 터미널에서 `claude`를 입력합니다.

**방법 2. 사이드바 패널 사용**  
설치 후 왼쪽 사이드바에 Claude Code 아이콘이 생깁니다.  
아이콘을 클릭하면 에디터 옆에 대화창이 열립니다.

> 💡 두 방법 모두 같은 Claude Code입니다. 편한 방법을 사용하세요.

---

## 8-3. 실습: 전체 삭제 버튼 추가하기

할 일 앱에 모든 항목을 한 번에 지우는 버튼을 추가해 봅시다.

Claude Code 대화창에 아래 내용을 입력하세요:

```
할 일 목록을 전체 삭제하는 버튼을 추가해줘. 버튼은 목록 아래쪽에 위치하고, 누르면 확인 메시지를 보여줘
```

Claude Code가 파일을 수정합니다. 어떤 부분을 바꿨는지 설명도 해 줍니다.

---

## 8-4. 결과 확인하기

브라우저에서 앱을 새로고침(`Command(⌘) + R`)해서 확인합니다.

"전체 삭제" 버튼이 보이고, 클릭하면 확인 메시지가 나타나면 성공입니다. 🎉

---

## 8-5. Cursor AI vs Claude Code — 뭐가 다른가요?

| | Cursor AI | Claude Code |
|---|---|---|
| **위치** | 에디터 오른쪽 패널 | 터미널 또는 사이드바 |
| **강점** | 현재 열린 파일 빠르게 수정 | 여러 파일을 연결해서 작업 |
| **사용법** | 코드 선택 후 요청 | 대화 형식으로 요청 |

둘 다 사용하면 더 강력합니다. 빠른 수정은 Cursor AI, 여러 파일에 걸친 작업은 Claude Code가 효과적입니다.

---

## FAQ

**Q. 사이드바에 Claude Code 아이콘이 안 보여요.**  
Cursor를 완전히 종료 후 다시 시작해 보세요. 그래도 없으면 Extensions에서 Claude Code가 설치됐는지 확인하세요.

**Q. 터미널 방법과 사이드바 방법 중 어느 게 좋나요?**  
사이드바가 코드와 대화창을 동시에 보여서 더 편리합니다. 처음에는 사이드바를 추천합니다.

---

이전 단계: [← 터미널로 Claude Code 사용하기](07.터미널로-Claude-Code-사용하기.md)  
[← 목차로 돌아가기](README.md)

---

**Claude Code와 함께 무엇이든 만들어보세요! 🚀**
```

- [ ] **Step 2: 내용 검토**

아래 기준으로 확인한다:
- 사이드바 아이콘 위치 설명이 충분히 명확한지
- Cursor AI vs Claude Code 비교표가 입문자에게 와닿는지
- FAQ가 실제로 발생할 오류를 커버하는지

- [ ] **Step 3: 커밋**

```bash
git add 08.Cursor에서-Claude-Code-사용하기.md
git commit -m "docs: 08. Cursor에서 Claude Code 사용하기 챕터 추가"
```

---

## Task 4: README.md 목차 업데이트

**Files:**
- Modify: `README.md`

- [ ] **Step 1: README.md 기존 목차 확인**

현재 목차 마지막 줄 확인:
```
5. [브라우저에서 확인하기](05.브라우저에서-확인하기.md)
```

- [ ] **Step 2: 목차에 항목 3개 추가**

위 줄 바로 다음에 아래 내용을 추가한다:

```markdown
6. [Claude Code 시작하기](06.Claude-Code-시작하기.md)
7. [터미널로 Claude Code 사용하기](07.터미널로-Claude-Code-사용하기.md)
8. [Cursor에서 Claude Code 사용하기](08.Cursor에서-Claude-Code-사용하기.md)
```

- [ ] **Step 3: 커밋**

```bash
git add README.md
git commit -m "docs: README 목차에 Claude Code 챕터 (06~08) 추가"
```
