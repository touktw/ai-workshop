# Cursor 웹 개발 입문 가이드 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 비개발자 맥북 사용자가 Cursor로 할 일 목록 웹앱을 완성할 수 있도록 한국어 단계별 가이드 문서 모음을 작성한다.

**Architecture:** README.md + 5개 챕터 파일 + images/ 폴더 구조. 각 챕터는 독립된 단계이며 선형 순서로 읽는다. 모든 명령어는 코드블록, 팁/주의는 인용 박스, 스크린샷은 placeholder 이미지 태그 사용.

**Tech Stack:** Markdown, GitHub-flavored MD (링크, 코드블록, 인용, 이미지)

---

### Task 1: images 폴더 및 README.md 작성

**Files:**
- Create: `images/.gitkeep`
- Create: `README.md`

- [ ] **Step 1: images 폴더 생성**

```bash
mkdir -p images
touch images/.gitkeep
```

- [ ] **Step 2: README.md 작성**

`README.md` 전체 내용:

```markdown
# 🖥️ Cursor로 시작하는 웹 개발 입문

## 소개

개발 지식이 전혀 없어도 괜찮습니다.  
이 가이드는 Cursor AI 코드 에디터를 활용해서  
**맥북 환경 세팅부터 첫 번째 웹앱(할 일 목록) 완성까지** 단계별로 안내합니다.

Cursor의 AI 기능 덕분에 코드를 직접 작성하지 않아도 됩니다.  
AI에게 원하는 것을 설명하면, AI가 코드를 만들어 줍니다.

## 준비물

- 맥북 (macOS 12 Monterey 이상 권장)
- 인터넷 연결
- 예상 소요 시간: 약 2~3시간

## 목차

1. [Cursor 가입 및 설치하기](01.커서-가입-및-설치.md)
2. [맥 개발환경 세팅하기](02.맥-개발환경-세팅.md) — 터미널, Homebrew, Node.js/npm
3. [첫 번째 프로젝트 만들기](03.첫-프로젝트-만들기.md)
4. [할 일 목록 앱 만들기](04.할일목록-앱-만들기.md)
5. [브라우저에서 확인하기](05.브라우저에서-확인하기.md)

---

> 💡 **막히는 부분이 있으면?**  
> 각 챕터 하단에 자주 묻는 질문(FAQ)을 참고하세요.
```

- [ ] **Step 3: 커밋**

```bash
git add README.md images/.gitkeep
git commit -m "README 및 images 폴더 추가"
```

---

### Task 2: 01.커서-가입-및-설치.md 작성

**Files:**
- Create: `01.커서-가입-및-설치.md`

- [ ] **Step 1: 파일 작성**

`01.커서-가입-및-설치.md` 전체 내용:

```markdown
# 1단계: Cursor 가입 및 설치하기

> 이 챕터에서 할 것: Cursor 계정을 만들고, 맥북에 설치한 뒤 처음 실행해봅니다.

---

## 1-1. Cursor란?

Cursor는 AI가 내장된 코드 에디터입니다.  
코드 작성 경험이 없어도 AI에게 원하는 것을 말하면 코드를 만들어 줍니다.

![Cursor 소개 화면](images/01-cursor-intro.png)

---

## 1-2. 계정 만들기

1. 브라우저에서 [cursor.com](https://cursor.com) 에 접속합니다.
2. 우측 상단 **Sign Up** 버튼을 클릭합니다.
3. Google 계정 또는 이메일로 가입합니다.

![cursor.com 홈페이지](images/01-cursor-homepage.png)

> 💡 **이미 GitHub 계정이 있다면?**  
> GitHub으로 로그인해도 됩니다.

---

## 1-3. 다운로드 및 설치

1. 로그인 후 **Download for Mac** 버튼을 클릭합니다.
2. 다운로드된 `.dmg` 파일을 더블클릭합니다.
3. Cursor 아이콘을 **Applications** 폴더로 드래그합니다.

![Cursor 설치 화면](images/01-cursor-install.png)

> ⚠️ **"확인되지 않은 개발자" 경고가 뜨면?**  
> 시스템 환경설정 → 보안 및 개인 정보 보호 → **확인 없이 열기** 클릭

---

## 1-4. 처음 실행하기

1. Launchpad 또는 Applications 폴더에서 **Cursor**를 실행합니다.
2. 로그인 화면이 뜨면 가입한 계정으로 로그인합니다.
3. 아래와 같은 화면이 보이면 설치 완료입니다. 🎉

![Cursor 첫 실행 화면](images/01-cursor-first-run.png)

---

## FAQ

**Q. 유료인가요?**  
무료 플랜으로 시작할 수 있습니다. 이 가이드는 무료 플랜 기준으로 작성되었습니다.

**Q. 설치 중 오류가 발생해요.**  
macOS 버전을 확인해보세요. macOS 12 이상이 필요합니다.  
시스템 환경설정 → 일반 → 소프트웨어 업데이트에서 확인할 수 있습니다.

---

다음 단계: [맥 개발환경 세팅하기 →](02.맥-개발환경-세팅.md)
```

- [ ] **Step 2: 커밋**

```bash
git add 01.커서-가입-및-설치.md
git commit -m "01. Cursor 가입 및 설치 가이드 추가"
```

---

### Task 3: 02.맥-개발환경-세팅.md 작성

**Files:**
- Create: `02.맥-개발환경-세팅.md`

- [ ] **Step 1: 파일 작성**

`02.맥-개발환경-세팅.md` 전체 내용:

```markdown
# 2단계: 맥 개발환경 세팅하기

> 이 챕터에서 할 것: 터미널 사용법을 익히고, Homebrew와 Node.js/npm을 설치합니다.

---

## 2-1. 터미널이란?

터미널은 컴퓨터에 명령을 직접 입력하는 도구입니다.  
마우스 클릭 대신 텍스트 명령으로 작업합니다.

**터미널 여는 방법:**
1. 키보드에서 `Command(⌘) + Space`를 눌러 Spotlight를 엽니다.
2. `terminal`을 입력하고 Enter를 누릅니다.

![터미널 실행 화면](images/02-terminal-open.png)

> 💡 **터미널이 무섭게 느껴지나요?**  
> 이 가이드에서 사용하는 명령어는 복사해서 붙여넣으면 됩니다. 직접 외울 필요 없습니다.

---

## 2-2. Homebrew 설치

Homebrew는 맥에서 개발 도구를 쉽게 설치하는 패키지 관리자입니다.

터미널을 열고 아래 명령어를 **복사해서 붙여넣기** 한 뒤 Enter를 누르세요:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

설치 중 맥북 비밀번호를 물어볼 수 있습니다. 입력 시 화면에 표시되지 않지만 정상입니다.

![Homebrew 설치 중](images/02-homebrew-install.png)

설치가 완료되면 아래 명령어로 확인합니다:

```bash
brew --version
```

아래와 비슷한 결과가 나오면 성공입니다:

```
Homebrew 4.x.x
```

> ⚠️ **Apple Silicon(M1/M2/M3) 맥북 사용자 주의**  
> 설치 완료 후 터미널에 아래 명령어를 추가로 실행하세요:
> ```bash
> echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
> eval "$(/opt/homebrew/bin/brew shellenv)"
> ```

---

## 2-3. Node.js 및 npm 설치

Node.js는 JavaScript를 실행하는 환경이고, npm은 패키지 설치 도구입니다.

```bash
brew install node
```

설치 완료 후 버전을 확인합니다:

```bash
node --version
npm --version
```

아래와 비슷한 결과가 나오면 성공입니다:

```
v20.x.x
10.x.x
```

![Node.js 설치 확인](images/02-node-version.png)

---

## FAQ

**Q. 명령어를 입력했는데 "command not found"가 떠요.**  
Homebrew 설치가 완료되지 않은 것일 수 있습니다. 2-2 단계를 다시 시도해보세요.

**Q. 설치에 너무 오래 걸려요.**  
인터넷 속도에 따라 5~15분 걸릴 수 있습니다. 기다려 주세요.

---

이전 단계: [← Cursor 가입 및 설치하기](01.커서-가입-및-설치.md)  
다음 단계: [첫 번째 프로젝트 만들기 →](03.첫-프로젝트-만들기.md)
```

- [ ] **Step 2: 커밋**

```bash
git add 02.맥-개발환경-세팅.md
git commit -m "02. 맥 개발환경 세팅 가이드 추가"
```

---

### Task 4: 03.첫-프로젝트-만들기.md 작성

**Files:**
- Create: `03.첫-프로젝트-만들기.md`

- [ ] **Step 1: 파일 작성**

`03.첫-프로젝트-만들기.md` 전체 내용:

```markdown
# 3단계: 첫 번째 프로젝트 만들기

> 이 챕터에서 할 것: 프로젝트 폴더를 만들고 Cursor에서 열어봅니다.

---

## 3-1. 프로젝트 폴더 만들기

터미널을 열고 아래 명령어를 실행해 바탕화면에 프로젝트 폴더를 만듭니다:

```bash
mkdir ~/Desktop/my-todo-app
```

> 💡 `mkdir`은 폴더를 만드는 명령어입니다. `~/Desktop`은 바탕화면을 의미합니다.

---

## 3-2. Cursor에서 폴더 열기

1. Cursor를 실행합니다.
2. 상단 메뉴 **File → Open Folder**를 클릭합니다.
3. 바탕화면에서 `my-todo-app` 폴더를 선택하고 **Open**을 클릭합니다.

![Cursor에서 폴더 열기](images/03-cursor-open-folder.png)

---

## 3-3. 첫 번째 파일 만들기

Cursor 왼쪽 파일 탐색기에서 **새 파일(+)** 버튼을 클릭합니다.  
파일 이름을 `index.html`로 입력하고 Enter를 누릅니다.

![새 파일 생성](images/03-cursor-new-file.png)

> 💡 `index.html`은 웹 페이지의 시작 파일입니다. 브라우저는 폴더를 열 때 이 파일을 가장 먼저 찾습니다.

---

## 3-4. 파일 구조 이해하기

완성된 프로젝트의 파일 구조는 아래와 같습니다:

```
my-todo-app/
├── index.html    ← 웹 페이지 구조
├── style.css     ← 디자인/색상
└── app.js        ← 기능(버튼 클릭 등)
```

지금은 `index.html`만 있어도 됩니다. 나머지는 다음 챕터에서 AI가 만들어 줍니다.

---

## FAQ

**Q. Cursor에서 폴더가 보이지 않아요.**  
File → Open Folder를 다시 시도하거나, 바탕화면에서 `my-todo-app` 폴더가 있는지 확인해보세요.

---

이전 단계: [← 맥 개발환경 세팅하기](02.맥-개발환경-세팅.md)  
다음 단계: [할 일 목록 앱 만들기 →](04.할일목록-앱-만들기.md)
```

- [ ] **Step 2: 커밋**

```bash
git add 03.첫-프로젝트-만들기.md
git commit -m "03. 첫 번째 프로젝트 만들기 가이드 추가"
```

---

### Task 5: 04.할일목록-앱-만들기.md 작성

**Files:**
- Create: `04.할일목록-앱-만들기.md`

- [ ] **Step 1: 파일 작성**

`04.할일목록-앱-만들기.md` 전체 내용:

```markdown
# 4단계: 할 일 목록 앱 만들기

> 이 챕터에서 할 것: Cursor AI에게 할 일 목록 웹앱을 만들어 달라고 요청하고, 코드를 이해해봅니다.

---

## 4-1. Cursor AI 채팅 열기

Cursor에서 AI와 대화하려면 채팅 패널을 엽니다.

- 단축키: `Command(⌘) + L`
- 또는 우측 상단 채팅 아이콘 클릭

![Cursor AI 채팅 패널](images/04-cursor-chat.png)

---

## 4-2. AI에게 앱 만들어달라고 요청하기

채팅창에 아래 내용을 **복사해서 붙여넣기** 하고 Enter를 누르세요:

```
index.html, style.css, app.js 파일을 만들어줘.
할 일 목록 웹앱을 만들고 싶어.
기능은 이래:
- 할 일 입력 후 추가 버튼 클릭하면 목록에 추가됨
- 각 항목 옆에 완료 체크박스 있음
- 완료된 항목은 취소선으로 표시됨
- 삭제 버튼으로 항목 삭제 가능
디자인은 깔끔하고 심플하게 해줘.
```

> 💡 AI에게 요청할 때는 원하는 것을 최대한 구체적으로 설명할수록 좋습니다.

![AI 요청 화면](images/04-cursor-ai-request.png)

---

## 4-3. AI가 만든 코드 적용하기

AI가 코드를 생성하면 각 파일 코드 블록 우측 상단의 **Apply** 버튼을 클릭합니다.

1. `index.html` 코드 → Apply 클릭
2. `style.css` 코드 → Apply 클릭
3. `app.js` 코드 → Apply 클릭

![AI 코드 적용](images/04-cursor-apply.png)

> 💡 **Apply 버튼이 안 보이면?**  
> 코드 블록 위에 마우스를 올리면 버튼이 나타납니다.

파일 저장은 `Command(⌘) + S`로 합니다.

---

## 4-4. 코드 간단히 이해하기

AI가 만든 코드가 어떤 역할을 하는지 간단히 살펴봅니다.

| 파일 | 역할 |
|------|------|
| `index.html` | 웹 페이지의 뼈대. 버튼, 입력창, 목록의 위치를 정의 |
| `style.css` | 색상, 크기, 폰트 등 디자인 담당 |
| `app.js` | 버튼 클릭, 항목 추가/삭제 등 기능 담당 |

> 💡 코드를 완전히 이해하지 않아도 됩니다. AI에게 "이 코드가 무슨 뜻이야?"라고 물어보면 설명해줍니다.

---

## 4-5. AI에게 수정 요청해보기

앱이 마음에 들지 않는 부분이 있으면 AI에게 다시 요청할 수 있습니다.

예시:
```
배경색을 연한 파란색으로 바꿔줘
```

```
완료된 항목의 글자색을 회색으로 바꿔줘
```

---

## FAQ

**Q. AI가 코드를 만들었는데 Apply 버튼이 없어요.**  
코드 블록 위에 마우스 커서를 올려보세요. 또는 코드를 직접 복사해서 해당 파일에 붙여넣기 해도 됩니다.

**Q. 파일이 저장되지 않는 것 같아요.**  
`Command(⌘) + S`로 각 파일을 저장하거나, File → Save All로 한 번에 저장하세요.

---

이전 단계: [← 첫 번째 프로젝트 만들기](03.첫-프로젝트-만들기.md)  
다음 단계: [브라우저에서 확인하기 →](05.브라우저에서-확인하기.md)
```

- [ ] **Step 2: 커밋**

```bash
git add 04.할일목록-앱-만들기.md
git commit -m "04. 할 일 목록 앱 만들기 가이드 추가"
```

---

### Task 6: 05.브라우저에서-확인하기.md 작성

**Files:**
- Create: `05.브라우저에서-확인하기.md`

- [ ] **Step 1: 파일 작성**

`05.브라우저에서-확인하기.md` 전체 내용:

```markdown
# 5단계: 브라우저에서 확인하기

> 이 챕터에서 할 것: 만든 웹앱을 브라우저에서 열어보고, Live Server로 실시간 미리보기를 설정합니다.

---

## 5-1. index.html 브라우저로 열기

가장 간단한 방법입니다.

1. Finder에서 바탕화면 → `my-todo-app` 폴더를 엽니다.
2. `index.html` 파일을 더블클릭합니다.
3. 기본 브라우저에서 웹앱이 열립니다. 🎉

![브라우저에서 앱 확인](images/05-browser-open.png)

> 💡 주소창에 `file:///...`로 시작하는 주소가 보이면 정상입니다.

---

## 5-2. Live Server 설치하기 (코드 수정 시 자동 새로고침)

코드를 수정할 때마다 브라우저를 새로고침하는 것은 번거롭습니다.  
Live Server 확장을 설치하면 코드 저장 시 자동으로 새로고침됩니다.

1. Cursor 왼쪽 메뉴에서 확장(Extensions) 아이콘을 클릭합니다.
2. 검색창에 `Live Server`를 입력합니다.
3. **Live Server** (작성자: Ritwick Dey)를 찾아 **Install**을 클릭합니다.

![Live Server 설치](images/05-live-server-install.png)

---

## 5-3. Live Server로 실행하기

1. `index.html` 파일을 Cursor에서 엽니다.
2. 우측 하단의 **Go Live** 버튼을 클릭합니다.
3. 브라우저가 자동으로 열리며 웹앱이 표시됩니다.

![Go Live 버튼](images/05-go-live.png)

이제 코드를 수정하고 `Command(⌘) + S`로 저장하면 브라우저가 자동으로 새로고침됩니다.

---

## 5-4. 완성! 🎉

할 일 목록 앱을 직접 사용해보세요:

- [ ] 할 일 입력 후 추가 버튼 클릭
- [ ] 체크박스로 완료 표시
- [ ] 삭제 버튼으로 항목 제거

![완성된 할 일 목록 앱](images/05-todo-app-complete.png)

---

## 더 나아가기

이제 기본기를 익혔습니다. 다음 단계로 도전해보세요:

- Cursor AI에게 새로운 기능을 요청해보기 (예: "할 일 개수를 상단에 표시해줘")
- 디자인 변경 요청해보기
- 완성된 앱을 Vercel로 배포해서 인터넷에 올려보기

---

## FAQ

**Q. 브라우저에서 열었는데 빈 화면이 나와요.**  
`index.html`이 저장되어 있는지 확인하세요. `Command(⌘) + S`로 저장 후 새로고침합니다.

**Q. Go Live 버튼이 보이지 않아요.**  
Cursor를 재시작하거나 Live Server 확장이 제대로 설치되었는지 확인하세요.

---

이전 단계: [← 할 일 목록 앱 만들기](04.할일목록-앱-만들기.md)  

---

**가이드를 완료하셨습니다! 수고하셨습니다. 🎊**
```

- [ ] **Step 2: 커밋**

```bash
git add 05.브라우저에서-확인하기.md
git commit -m "05. 브라우저에서 확인하기 가이드 추가"
```

---

### Task 7: 스펙 업데이트 및 최종 커밋

**Files:**
- Modify: `docs/superpowers/specs/2026-04-23-cursor-web-guide-design.md`

- [ ] **Step 1: 스펙 파일의 파일명 규칙 업데이트**

스펙 내 파일명을 확정된 한글 + `.` 구분자 형식으로 수정:

```
01.커서-가입-및-설치.md
02.맥-개발환경-세팅.md
03.첫-프로젝트-만들기.md
04.할일목록-앱-만들기.md
05.브라우저에서-확인하기.md
```

- [ ] **Step 2: 최종 커밋**

```bash
git add docs/
git commit -m "스펙 파일명 한글 형식으로 업데이트"
```
