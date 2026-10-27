---
theme: ./slidev-themes/hossam
title: Markdown의 이해와 활용
layout: cover
---

# Markdown의 이해와 활용

기호 몇 개로 글에 제목, 목록, 표, 코드를 붙이는 법

<p class="sub">이광호 강사 · VS Code 실습</p>

---

## 마크다운이란 — AI와 주고받는 글의 서식

마크다운은 **기호로 서식을 표시하는 글쓰기 규칙**이다. AI를 쓸 때는 사람과 AI가 같이 읽는 공용 서식이 된다.

- **AI의 답이 마크다운이다.** ChatGPT·Claude 답변의 제목, 굵은 글씨, 표, 코드 상자는 모두 마크다운이 그려진 모습이다
- **프롬프트를 마크다운으로 쓰면 AI가 더 정확히 알아듣는다.** 지시와 자료가 구분되기 때문이다
- **원하는 결과 모양을 정해 줄 수 있다.** "표로", "체크리스트로"라고 하면 그대로 붙여 쓸 수 있는 결과가 온다
- **AI가 읽는 규칙서도 마크다운 파일이다.** Claude Code의 `CLAUDE.md`, 코딩 에이전트의 `AGENTS.md`, 프로젝트 `README.md`

<Callout kind="warn">
마크다운이 그려지지 않는 곳(문자, 카톡, 일반 메일)에 AI 답을 붙이면 <code>**</code>, <code>#</code> 같은 기호가 그대로 보인다. 그럴 때는 "서식 없이 평문으로 써 줘"라고 따로 요청한다.
</Callout>

---

### AI 시대, 마크다운의 의미

"가벼운 서식 문법"에서 "사람과 AI의 공용어"로

<Grid cols="2">
<Card sm acc k="01" t="🤖 LLM의 모국어">

- README·기술 문서·Q&A 등 학습 데이터에 마크다운이 풍부하다
- ChatGPT·Claude는 마크다운으로 읽고 마크다운으로 답한다
- 프롬프트를 제목과 목록으로 구조를 갖춰 전달하면 AI가 더 정확히 이해한다

</Card>
<Card sm acc k="02" t="👀 사람도 기계도 그대로 읽는 텍스트">

- 렌더링 없이도 읽히는 평문이라 특정 프로그램에 묶이지 않는다
- Git으로 버전을 관리하고 변경 내역을 비교한다
- 어디든 복사해 그대로 쓴다

</Card>
<Card sm acc k="03" t="⚙️ AI 에이전트의 설정 언어">

- `CLAUDE.md` · `AGENTS.md` · `SKILL.md` · 시스템 프롬프트
- AI에게 주는 지시·규칙·기억이 전부 마크다운 파일이다
- "문서를 쓰는 일" = "AI를 프로그래밍하는 일"

</Card>
<Card sm acc k="04" t="📦 콘텐츠의 원본 (Source of Truth)">

- 내용은 마크다운 한 벌로 작성한다
- PPT·PDF·HTML·Notion 변환은 AI에게 맡긴다
- 서식은 선택지일 뿐, 남는 자산은 구조를 가진 텍스트다

</Card>
</Grid>

<Callout kind="real">
마크다운은 서식 도구가 아니라 "구조를 가진 생각"을 담는 최소 단위다. AI 시대의 글쓰기, 지시, 지식 관리가 모두 여기서 출발한다.
</Callout>

---

### 프롬프트를 마크다운으로 쓰면

<Grid cols="2">
<div>

<div class="kicker">평문 프롬프트</div>

```text
아래 데이터에서 결측치를 찾아서
표로 정리하고 원인도 추측해 줘
이름 나이 철수 비어있음 영희 21
```

- 어디까지가 지시고 어디부터가 자료인지 흐리다
- 할 일이 한 문장에 섞여 하나를 빠뜨리기 쉽다

</div>
<div>

<div class="kicker">마크다운 프롬프트</div>

````md
## 할 일
- 결측치를 찾아 표로 정리
- 원인을 한 줄씩 추측

## 데이터
```csv
이름,나이
철수,
영희,21
```

## 출력 형식
| 열 | 결측 수 | 원인 |
````

</div>
</Grid>

<Callout kind="real" title="이렇게 쓰면 좋은 점">

- **지시와 자료가 섞이지 않는다.** 코드 상자가 자료의 시작과 끝을 표시한다
- **할 일을 빠뜨리지 않는다.** 목록 한 줄이 할 일 하나다
- **결과 모양을 미리 보여 줄 수 있다.** 표 머리글만 적어 두면 그 모양대로 채워 온다
- **다시 쓰기 쉽다.** `.md` 파일로 저장해 두고 자료만 바꿔 쓴다

</Callout>

---

### 기호로 하는 서식

- `#` 을 붙이면 제목, `**` 로 감싸면 굵은 글씨가 된다
- 파일은 그냥 텍스트라서 메모장에서도 열리고 미리보기를 켜면 서식이 입혀진다

<Callout kind="eli5">
문자 메시지에 ㅋㅋ나 ^^를 붙이면 말투가 달라 보이는 것과 비슷하다. 글자 몇 개를 덧붙이는 것만으로 "여기는 제목", "여기는 강조"라고 표시한다.
</Callout>

<Callout kind="real">
GitHub의 README, 주피터 노트북의 설명 셀, 노션도 모두 마크다운으로 쓴다. 한 번 익혀 두면 여기저기서 그대로 쓸 수 있다.
</Callout>

---

## 1. VS Code 준비 — Visual Studio Code 설치하기

- **Visual Studio Code**는 Microsoft가 만들어 무료로 배포하는 IDE(코딩 작업 통합 프로그램)다
- 여러 프로그래밍 언어를 지원해서 IDE 중에서 가장 인기가 높다
- 익스텐션(확장팩)을 설치해 기능을 늘릴 수 있다

<div class="fill-img"><img src="./img/002/vscode-overview.png" alt="Visual Studio Code에서 코드를 편집하는 화면" /></div>

---

### 1.1 VS Code 내려받기

<Steps>
<li><a href="https://code.visualstudio.com">https://code.visualstudio.com</a> 에 접속한다</li>
<li>화면의 <b>Download</b> 버튼을 눌러 설치 프로그램을 내려받는다</li>
<li>내려받은 프로그램을 실행해 설치를 진행한다 (특별한 설정은 없다)</li>
</Steps>

<div class="fill-img"><img src="./img/002/vscode-download.png" alt="VS Code 홈페이지의 Download 버튼. 누르면 페이지가 이동하고 2~3초 뒤 다운로드가 시작된다" /></div>

---

### 1.2 VS Code 설치 과정

<Grid cols="3">
<div>

<div class="kicker">1. 사용권 계약 동의 → 다음</div>

<img src="./img/002/vscode-install-step1.png" alt="사용권 계약에서 동의합니다를 고르고 다음 누르기" style="max-height: 190px;" />

</div>
<div>

<div class="kicker">2. 설치 위치 확인 → 다음</div>

<img src="./img/002/vscode-install-step2.png" alt="설치 위치를 그대로 두고 다음 누르기" style="max-height: 190px;" />

</div>
<div>

<div class="kicker">3. 시작 메뉴 폴더 → 다음</div>

<img src="./img/002/vscode-install-step3.png" alt="시작 메뉴 폴더를 그대로 두고 다음 누르기" style="max-height: 190px;" />

</div>
<div>

<div class="kicker">4. 추가 작업 모두 체크 → 다음</div>

<img src="./img/002/vscode-install-step4.png" alt="바탕 화면 바로가기, Code로 열기, PATH에 추가 항목을 모두 체크하고 다음 누르기" style="max-height: 190px;" />

</div>
<div>

<div class="kicker">5. 설치 누르기</div>

<img src="./img/002/vscode-install-step5.png" alt="설치 준비 완료 화면에서 설치 누르기" style="max-height: 190px;" />

</div>
<div>

<div class="kicker">6. 설치 진행 중</div>

<img src="./img/002/vscode-install-step6.png" alt="설치 진행 막대가 차오르는 화면" style="max-height: 190px;" />

</div>
</Grid>

---

### 1.3 설치 종료 및 실행

설치 프로그램에서 **종료**를 누르면 Visual Studio Code가 바로 실행된다.

<div class="fill-img"><div class="fill-in">
<figure><div class="pic"><img src="./img/002/vscode-install-finish.png" alt="설치 마법사 완료 화면에서 Visual Studio Code 실행에 체크하고 종료 누르기" /></div></figure>
<figure><div class="pic"><img src="./img/002/vscode-first-run.png" alt="처음 실행된 VS Code의 Welcome 화면" /></div></figure>
</div></div>

---

### 1.4 익스텐션 설치 — 한국어

익스텐션은 VS Code의 기능을 늘리기 위해 설치하는 작은 프로그램이다.

<div class="fill-img"><div class="fill-in">
<div class="fill-text">

<Steps>
<li>왼쪽의 익스텐션 아이콘(네모 네 개)을 누른다</li>
<li>검색창에 <b>Korean</b>을 입력한다</li>
<li>Microsoft가 만든 <b>Korean Language Pack</b>을 설치한다</li>
<li>오른쪽 아래에 뜨는 <b>Change Language and Restart</b>를 눌러 다시 실행한다</li>
</Steps>

</div>
<figure style="flex-grow: 1.5"><div class="pic"><img src="./img/002/ext-korean.png" alt="익스텐션 창에서 Korean을 검색해 한국어 팩을 설치하고 재시작 버튼 누르기" /></div></figure>
</div></div>

---

### 1.5 환경 설정 — 글자 크기

기본 글자 크기가 조금 작으니 **16**으로 바꾼다. 코딩하면서 내 눈에 맞게 다시 조절해도 된다.

<div class="fill-img"><div class="fill-in">
<div class="fill-text">

<Steps>
<li>왼쪽 아래 톱니바퀴를 누른다</li>
<li><b>설정</b>을 고른다</li>
<li><b>Editor: Font Size</b> 칸에 <code>16</code>을 입력한다</li>
</Steps>

</div>
<figure style="flex-grow: 1.5"><div class="pic"><img src="./img/002/setting-font-size.png" alt="톱니바퀴 → 설정 → Editor: Font Size에 16 입력" /></div></figure>
</div></div>

---

### 1.6 환경 설정 — 아이콘 테마 설치

- 검색해 보면 여러 아이콘 테마가 있다. 가장 많이 쓰는 것은 **Material Icon Theme**다
- 설치가 끝나면 화면 위쪽에 테마를 고르는 목록이 뜬다

<div class="fill-img"><div class="fill-in">
<div class="fill-text">

<Steps>
<li>익스텐션 아이콘을 누른다</li>
<li>검색창에 <b>Icon</b>을 입력한다</li>
<li><b>Material Icon Theme</b>을 설치한다</li>
</Steps>

</div>
<figure style="flex-grow: 1.5"><div class="pic"><img src="./img/002/ext-material-icon.png" alt="익스텐션 창에서 Icon을 검색해 Material Icon Theme 설치하기" /></div></figure>
</div></div>

---

### 1.7 환경 설정 — 아이콘 테마 고르기

이미 설치된 아이콘 테마 중에서 고를 때는 아래 순서로 연다.

<div class="fill-img"><div class="fill-in">
<figure><div class="kicker">톱니바퀴 → 테마 → 파일 아이콘 테마</div><div class="pic"><img src="./img/002/icon-theme-menu.png" alt="톱니바퀴 메뉴에서 테마, 파일 아이콘 테마 순서로 열기" /></div></figure>
<figure><div class="kicker">목록에서 Material Icon Theme 선택</div><div class="pic"><img src="./img/002/icon-theme-select.png" alt="파일 아이콘 테마 목록에서 Material Icon Theme 고르기" /></div></figure>
</div></div>

---

### 1.8 환경 설정 — 아이콘 테마 확인

기본 상태에서는 폴더와 파일을 구분하기 어렵지만, 아이콘 테마를 적용하면 **파일 종류가 한눈에 보인다**.

<div class="fill-img"><div class="fill-in">
<figure><div class="kicker">설치 전</div><div class="pic"><img src="./img/002/icon-theme-before.png" alt="아이콘 테마 적용 전 탐색기. 폴더와 파일이 글자만으로 구분된다" /></div></figure>
<figure><div class="kicker">설치 후</div><div class="pic"><img src="./img/002/icon-theme-after.png" alt="아이콘 테마 적용 후 탐색기. 폴더와 파일마다 종류별 아이콘이 붙는다" /></div></figure>
</div></div>

---

### 1.9 환경 설정 — 색상 테마

데이터 분석 코드는 **밝은 테마**에서 더 잘 읽히므로 바꾸는 것을 추천한다. 취향에 따라 어두운 테마를 써도 된다.

<div class="fill-img"><div class="fill-in">
<figure><div class="kicker">톱니바퀴 → 테마 → 색 테마</div><div class="pic"><img src="./img/002/color-theme-menu.png" alt="톱니바퀴 메뉴에서 테마, 색 테마 순서로 열기" /></div></figure>
<figure><div class="kicker">밝게(Visual Studio) 선택</div><div class="pic"><img src="./img/002/color-theme-select.png" alt="색 테마 목록에서 밝게(Visual Studio) 고르기" /></div></figure>
</div></div>

---

### 1.10 VS Code 삭제하기 — 설정 앱 열기

윈도우의 **설정** 앱을 실행하고 **앱**으로 들어간다.

<div class="fill-img"><img src="./img/002/uninstall-settings-app.png" alt="윈도우 설정 앱에서 앱 메뉴 선택" /></div>

---

### 1.11 VS Code 삭제하기 — 프로그램 제거

**앱 및 기능** 목록에서 **Microsoft Visual Studio Code**를 찾아 **제거**를 누른다.

<div class="fill-img"><img src="./img/002/uninstall-apps.png" alt="앱 및 기능 목록에서 Microsoft Visual Studio Code 제거" /></div>

---

### 1.12 VS Code 삭제하기 — 설정 폴더 지우기

<div class="fill-img"><div class="fill-in">
<div class="fill-text">

<Steps>
<li>사용자 홈 폴더(<code>C:\사용자\계정명</code> 또는 <code>C:\Users\계정명</code>)를 연다</li>
<li><code>.vscode</code> 폴더를 삭제한다</li>
</Steps>

<Callout kind="warn">
프로그램만 지우면 설정과 익스텐션이 이 폴더에 남는다. 다시 설치했을 때 예전 문제가 그대로 따라오지 않게 <b>반드시</b> 함께 지운다.
</Callout>

</div>
<figure style="flex-grow: 1.5"><div class="pic"><img src="./img/002/uninstall-vscode-folder.png" alt="사용자 홈 폴더에서 .vscode 폴더 삭제" /></div></figure>
</div></div>

---

### 1.13 마크다운을 위한 익스텐션 설치

| 확장 | 만든 사람 | 하는 일 |
|:--|:--|:--|
| Markdown All in One | Yu Zhang | 문법 강조, 단축키, 목차 자동 생성 |
| Markdown Preview Github Styling | Matt Bierner | 미리보기를 GitHub 화면처럼 보여 줌 |
| Ipynb PDF converter | leekh | 마크다운 파일을 pdf 문서로 변환 |

VS Code 왼쪽의 확장 아이콘(네모 네 개)을 누르고 이름으로 검색해 설치한다.

<Callout kind="tip" title="미리보기 여는 법">

- 옆 창에 띄우기: `Ctrl + K` 를 누른 뒤 `V` (Mac은 `Cmd + K` → `V`)
- 같은 창에서 바꿔 보기: `Ctrl + Shift + V` (Mac은 `Cmd + Shift + V`)

</Callout>

---

## 2. 마크다운 뷰어 설정 — 크롬으로 md 파일 보기

VS Code를 열지 않아도 `.md` 파일을 **더블클릭만으로** 서식이 입혀진 화면으로 볼 수 있게 만든다.

<Steps>
<li>크롬 웹 스토어에서 <b>Markdown Reader</b> 익스텐션을 설치한다</li>
<li>Markdown Reader가 내 컴퓨터의 파일을 읽을 수 있게 허용한다</li>
<li><code>.md</code> 파일의 기본 연결 프로그램을 <b>Chrome</b>으로 바꾼다</li>
<li>취향에 맞게 색상 테마를 고른다</li>
</Steps>

<Callout kind="warn">
이 설정은 반드시 <b>크롬(Chrome) 웹 브라우저</b>에서 진행한다. 엣지 등 다른 브라우저에서는 화면과 메뉴가 다르다.
</Callout>

---

### 2.1 크롬 웹 스토어 접속

구글에서 **"크롬 웹 스토어"**를 검색해 들어간다. (반드시 크롬 웹 브라우저 사용)

<div class="fill-img"><img src="./img/002/md-reader-webstore.png" alt="구글에서 크롬 웹 스토어를 검색해 접속하는 화면" /></div>

---

### 2.2 설치할 익스텐션 검색

크롬 웹 스토어에서 **"Markdown Reader"**를 검색한다.

<div class="fill-img"><img src="./img/002/md-reader-search.png" alt="크롬 웹 스토어 검색창에 Markdown Reader 입력" /></div>

---

### 2.3 익스텐션 설치

오른쪽 위의 **"Chrome에 추가"** 버튼을 누른다.

<div class="fill-img"><img src="./img/002/md-reader-install.png" alt="Markdown Reader 페이지에서 Chrome에 추가 버튼 누르기" /></div>

---

### 2.4 익스텐션 관리 페이지로 이동

설치가 끝나면 확장 프로그램 아이콘 → **Markdown Reader** 옆 점 세 개 → **확장 프로그램 관리**를 누른다.

<div class="fill-img"><img src="./img/002/md-reader-manage.png" alt="크롬 확장 프로그램 목록에서 Markdown Reader 메뉴를 열고 확장 프로그램 관리 누르기" /></div>

---

### 2.5 컴퓨터 파일 접근 허용

**파일 URL에 대한 액세스 허용** 옵션을 켠다. 이걸 켜야 내 컴퓨터의 md 파일을 열 수 있다.

<div class="fill-img"><img src="./img/002/md-reader-file-access.png" alt="Markdown Reader 세부정보에서 파일 URL에 대한 액세스 허용 켜기" /></div>

---

### 2.6 md 파일의 연결 프로그램 바꾸기

아무 md 파일이나 마우스 오른쪽 버튼으로 누르고 **연결 프로그램 → 다른 앱 선택**을 누른다.

<div class="fill-img"><img src="./img/002/md-open-with.png" alt="파일 탐색기에서 md 파일을 우클릭해 연결 프로그램, 다른 앱 선택 누르기" /></div>

---

### 2.7 항상 크롬으로 열기

목록에서 **Google Chrome**을 고르고 **항상**을 눌러 늘 크롬으로 열리게 한다. 목록에 크롬이 없으면 **PC에서 앱 선택**을 눌러 `C:\Program Files\Google\Chrome\Application\chrome.exe` 를 고른다.

<div class="fill-img"><img src="./img/002/md-open-with-chrome.png" alt="연결 프로그램 선택 창에서 Google Chrome을 고르고 항상 누르기. 크롬이 없으면 PC에서 앱 선택으로 chrome.exe 지정" /></div>

---

### 2.8 md 파일을 크롬으로 열어 보기

`*.md` 파일을 더블클릭했을 때 크롬에서 서식이 입혀진 화면으로 열리는지 확인한다.

<div class="fill-img"><img src="./img/002/md-open-in-chrome.png" alt="md 파일이 크롬에서 목차와 서식이 적용된 문서로 열린 화면" /></div>

---

### 2.9 색상 테마 설정 — 옵션 열기

md 파일을 연 상태에서 확장 프로그램 아이콘 → **Markdown Reader**를 눌러 옵션 화면을 연다.

<div class="fill-img"><img src="./img/002/md-reader-options-menu.png" alt="md 파일을 연 크롬에서 확장 프로그램 아이콘을 누르고 Markdown Reader 선택" /></div>

---

### 2.10 색상 테마 설정 — 테마 고르기

글자 크기, 밝은/어두운 테마, 코드 블록 테마를 **각자 취향에 맞춰** 설정한다.

<div class="fill-img"><img src="./img/002/md-reader-theme.png" alt="Markdown Reader 옵션 화면에서 테마와 글자 크기 고르기" /></div>

---

## 3. 마크다운 작성 규칙

기호 몇 개만 익히면 제목, 목록, 표, 코드, 수식까지 쓸 수 있다.

<Grid cols="3">
<Card sm k="문서 뼈대" t="3.1 ~ 3.7">

- 새 마크다운 파일 만들기
- 제목
- 본문과 줄바꿈
- 목록

</Card>
<Card sm k="글자와 연결" t="3.8 ~ 3.12">

- 글자 강조
- 링크 · 이미지
- 표
- 인용문과 구분선

</Card>
<Card sm k="특수 블록" t="3.13 ~ 3.20">

- 체크박스
- 코드 블록
- 수식
- 기호를 글자 그대로 쓰기

</Card>
</Grid>

<Callout kind="tip">
각 규칙은 왼쪽에 쓰는 법, 오른쪽에 미리보기로 보여 준다. VS Code에서 <code>Ctrl + K</code> → <code>V</code> 로 미리보기를 띄워 두고 따라 써 본다.
</Callout>

---

### 3.1 새 마크다운 파일 만들기

<Steps>
<li><code>파일 → 새 텍스트 파일</code>을 고른다. 단축키는 <code>Ctrl + N</code> (Mac은 <code>Cmd + N</code>)</li>
<li>저장(<code>Ctrl + S</code>)할 때 파일 이름 끝을 <code>.md</code> 로 정한다. 예: <code>note.md</code></li>
<li>오른쪽 아래 상태 표시줄에 <b>Markdown</b>이 보이면 준비 끝</li>
</Steps>

<Callout kind="warn">
확장자를 <code>.txt</code> 로 저장하면 미리보기도 문법 강조도 동작하지 않는다.
</Callout>

---

### 3.2 제목 — `#` 의 개수가 크기

````md
# 문서 제목 (가장 큼)
## 큰 단원
### 작은 단원
#### 더 작은 단원
##### 거의 본문 크기
###### 가장 작음
````

- `#` 다음에 **한 칸 띄우고** 제목을 쓴다. `#제목` 처럼 붙이면 제목이 되지 않는다
- 1개부터 6개까지 쓸 수 있다. 개수가 적을수록 크다
- `#` 하나짜리 제목은 보통 문서 맨 위에 한 번만 쓴다

<Callout kind="eli5">
책의 목차를 떠올리면 된다. <code>#</code> 은 책 제목, <code>##</code> 는 장, <code>###</code> 은 절이다.
</Callout>

---

### 3.3 본문과 줄바꿈

<Grid cols="2">
<div>

```md
그냥 쓰면 본문이 된다.

엔터를 한 번 치면
줄이 바뀌지 않고 이어 붙는다.

빈 줄을 하나 두면
새 문단이 된다.
```

</div>
<div>

<div class="kicker">미리보기</div>

그냥 쓰면 본문이 된다.

엔터를 한 번 치면
줄이 바뀌지 않고 이어 붙는다.

빈 줄을 하나 두면
새 문단이 된다.

<Callout kind="tip" title="문단은 그대로, 줄만 바꾸고 싶으면">
줄 끝에 스페이스를 두 칸 넣거나 <code>&lt;br&gt;</code> 를 쓴다.
</Callout>

</div>
</Grid>

---

### 3.4 순서 있는 목록

<Grid cols="2">
<div>

```md
1. 재료 준비
1. 물 끓이기
1. 면 넣기
1. 3분 기다리기
```

- `1.` 다음에 **한 칸 띄운다**
- 번호를 모두 `1.` 로 써도 화면에는 1, 2, 3, 4로 나온다.
  - `1., 2., 3., 4.` 형식으로 연속된 번호를 사용해도 무관하다.
  - VSCode가 숫자 자동완성 기능을 지원함
- 중간에 항목을 끼워 넣어도 번호를 고칠 필요가 없다

</div>
<div>

<div class="kicker">미리보기</div>

1. 재료 준비
2. 물 끓이기
3. 면 넣기
4. 3분 기다리기

</div>
</Grid>

---

### 3.5 목록 안에 목록 넣기

<Grid cols="2">
<div>

```md
1. 아침
    1. 세수
    1. 밥 먹기
1. 점심
    1. 수업
    1. 산책
```

- 하위 항목은 `Tab` 키(스페이스 4칸)로 **안쪽으로 밀어** 쓴다
- 위아래 항목과 들여쓰기 칸 수를 맞춘다

</div>
<div>

<div class="kicker">미리보기</div>

1. 아침
    1. 세수
    1. 밥 먹기
1. 점심
    1. 수업
    1. 산책

</div>
</Grid>

---

### 3.6 순서 없는 목록

<Grid cols="2">
<div>

```md
* 과일
    - 사과
    - 배
- 채소
    * 오이
    * 당근
```

- `*` 와 `-` 중 아무거나 써도 결과가 같다
- 기호 다음에 **한 칸 띄운다**
- 순서 있는 목록 안에 순서 없는 목록을 넣는 것도 된다

</div>
<div>

<div class="kicker">미리보기</div>

* 과일
    - 사과
    - 배
- 채소
    * 오이
    * 당근

</div>
</Grid>

---

### 3.7 두 목록을 섞어 쓰기

<Grid cols="2">
<div>

```md
1. 준비물
    * 노트북
    * 충전기
1. 실습 순서
    1. 파일 만들기
    1. 저장하기
```

<Callout kind="eli5">
큰 순서는 번호로, 그 안의 준비물처럼 순서가 상관없는 것은 점으로 적는다. 장보기 목록을 쓸 때와 같다.
</Callout>

</div>
<div>

<div class="kicker">미리보기</div>

1. 준비물
    * 노트북
    * 충전기
1. 실습 순서
    1. 파일 만들기
    1. 저장하기

</div>
</Grid>

---

### 3.8 글자 강조

<Grid cols="2">
<div>

```md
**굵게**

*기울임*

***굵게 + 기울임***

~~취소선~~

`인라인 코드`
```

- 기호로 글자를 **양쪽에서 감싼다**
- 인라인 코드는 문장 안에서 코드나 파일 이름을 보여 줄 때 쓴다

</div>
<div>

<div class="kicker">미리보기</div>

**굵게**

*기울임*

***굵게 + 기울임***

~~취소선~~

`인라인 코드`

<Callout kind="warn">
각 줄 사이에 빈 줄이 없으면 다섯 개가 한 줄로 이어 붙는다. 3.3 본문과 줄바꿈의 규칙이 여기에도 그대로 적용된다.
</Callout>

</div>
</Grid>

---

### 3.9 링크

```md
[구글](https://www.google.com) 에서 검색한다.
```

- 형식: `[화면에 보일 글자](주소)`
- 두 번째 방법은 주소를 글 아래쪽에 따로 모아 둔다. 같은 주소를 여러 번 쓸 때 편하다
- 큰따옴표 안의 글자는 마우스를 올렸을 때 뜨는 설명이다

<div class="kicker">미리보기</div>

[구글](https://www.google.com) 에서 검색한다.

---

### 3.10 이미지

```md
![고양이 사진](images/cat.png)
```

- 링크 앞에 **느낌표 `!`** 하나만 붙이면 이미지가 된다
- 대괄호 안 글자는 그림이 안 열릴 때 대신 보이는 설명이다
- 주소 자리에 인터넷 주소 대신 내 컴퓨터의 파일 경로를 써도 된다.
- md 파일이 있는 폴더를 기준으로 적는다

---

### 3.11 표

```md
| 이름 | 과목 | 점수 |
|:-----|:----:|-----:|
| 철수 | 수학 |   90 |
| 영희 | 영어 |  100 |
```

- `|` 로 칸을 나누고 둘째 줄의 `---` 로 제목 줄과 내용을 가른다
- 콜론 `:` 위치로 정렬을 정한다. `:---` 왼쪽, `:---:` 가운데, `---:` 오른쪽

<div class="kicker">미리보기</div>

| 이름 | 과목 | 점수 |
|:-----|:----:|-----:|
| 철수 | 수학 |   90 |
| 영희 | 영어 |  100 |

<Callout kind="tip">
칸 너비를 꼭 맞추지 않아도 표는 잘 나온다. 
</Callout>

---

### 3.12 인용문과 구분선

<Grid cols="2">
<div>

```md
> 아는 것이 힘이다.
>
> 기능은 인용문이지만, 실제로는 강조 박스를 만들 때 사용한다.
```

<div class="kicker">미리보기</div>

> 아는 것이 힘이다.
>
> 기능은 인용문이지만, 실제로는 강조 박스를 만들 때 사용한다.

</div>
<div>

```md
***
___
```

- 셋 중 아무거나 한 줄에 쓰면 가로 구분선이 된다. 셋째 방법은 하이픈 세 개(`---`)다

<div class="kicker">미리보기</div>

***

<Callout kind="warn">

- <code>---</code> 바로 위 줄에 글자가 붙어 있으면 그 글자가 제목으로 바뀐다. 
- 구분선 위아래는 빈 줄로 띄운다.

</Callout>

</div>
</Grid>

---

### 3.13 체크박스

<Grid cols="2">
<div>

```md
- [x] 확장 설치하기
- [x] md 파일 만들기
- [ ] 표 만들어 보기
- [ ] 수식 써 보기
```

- `- [ ]` 는 빈 칸, `- [x]` 는 체크된 칸
- 대괄호 안에 **스페이스 한 칸**이 있어야 빈 칸으로 인식된다

</div>
<div>

<div class="kicker">미리보기</div>

- [x] 확장 설치하기
- [x] md 파일 만들기
- [ ] 표 만들어 보기
- [ ] 수식 써 보기

<Callout kind="real">
할 일 목록이나 과제 제출 전 점검표를 이렇게 만든다. 
</Callout>

</div>
</Grid>

---

### 3.14 코드 블록

역따옴표(`` ` ``) 세 개로 코드를 위아래에서 감싸고 여는 쪽 뒤에 언어 이름을 쓴다. 역따옴표는 키보드 `1` 왼쪽, `~` 와 같은 키에 있다.

<Grid cols="2">
<div>

<div class="kicker">Python</div>

````md
```python
for i in range(3):
    print("Hello", i)
```
````

<div class="kicker">미리보기</div>

```python
for i in range(3):
    print("Hello", i)
```

</div>
<div>

<div class="kicker">SQL</div>

````md
```sql
SELECT name, score
FROM students
WHERE score >= 90
ORDER BY score DESC;
```
````

<div class="kicker">미리보기</div>

```sql
SELECT name, score
FROM students
WHERE score >= 90
ORDER BY score DESC;
```

</div>
</Grid>

---

### 3.15 언어 이름 적는 법

| 언어 | 적는 이름 |
|:--|:--|
| Python | `python` 또는 `py` |
| JavaScript | `javascript` 또는 `js` |
| HTML · CSS | `html` · `css` |
| SQL | `sql` |
| 터미널 명령 | `bash` 또는 `shell` |
| 데이터 파일 | `json` · `xml` · `yaml` |
| 마크다운 자체 | `markdown` 또는 `md` |

<Callout kind="eli5">

- 언어 이름은 "이건 파이썬이야"라고 알려 주는 이름표다. 
- 이름표를 보고 예약어, 문자열, 숫자에 각각 다른 색을 입힌다. 
- 이름을 빼면 코드는 나오지만 전부 한 가지 색이다.

</Callout>

---

### 3.16 수식 — 문장 안에 넣기

달러 기호 `$` 한 개로 감싸면 문장 속에 수식이 들어간다.

```md
이차방정식의 해는 $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$ 이다.
```

<div class="kicker">미리보기</div>

이차방정식의 해는 $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$ 이다.

<Callout kind="eli5">

- 수식은 LaTeX(레이텍)이라는 수식 전용 규칙으로 쓴다. 
- <code>\frac{위}{아래}</code> 는 분수, <code>\sqrt{}</code> 는 루트처럼 명령어 하나가 기호 하나다.

</Callout>

---

### 3.17 수식 — 따로 한 줄에 크게

- `$$` 두 개로 위아래를 감싸면 수식이 가운데에 크게 놓인다. 
- `&` 는 줄을 맞출 기준점, `\\` 는 줄바꿈이다.

```md
$$
\begin{aligned}
E &= mc^2 \\
F &= ma
\end{aligned}
$$
```

<div class="kicker">미리보기</div>

$$
\begin{aligned}
E &= mc^2 \\
F &= ma
\end{aligned}
$$

---

### 3.18 자주 쓰는 수학 기호

| 보이는 모양 | 쓰는 법 | 뜻 |
|:--:|:--|:--|
| $x^2$ | `x^2` | 제곱 (위첨자) |
| $x_2$ | `x_2` | 아래첨자 |
| $\bar{x}$ | `\bar{x}` | 평균 |
| $\sqrt{x}$ | `\sqrt{x}` | 제곱근 |
| $\frac{a}{b}$ | `\frac{a}{b}` | 분수 |
| $\sum$ | `\sum` | 모두 더하기 |
| $\log_{2}$ | `\log_{2}` | 로그 (밑이 2) |
| $\leq$ · $\geq$ | `\leq` · `\geq` | 작거나 같음 · 크거나 같음 |
| $\varepsilon$ | `\varepsilon` | 아주 작은 양수 (오차를 나타낼 때 자주 씀) |

<Callout kind="warn">

- 첨자가 두 글자 이상이면 중괄호로 묶는다. 
- `x^10` 은 $x^10$ 으로 보이고 `x^{10}` 이라고 써야 $x^{10}$ 이 된다.

</Callout>

---

### 3.19 통계에서 쓰는 기호

| 기호 | 쓰는 법 | 뜻 |
|:--:|:--|:--|
| $\Omega$ | `\Omega` | 모집단 (조사하고 싶은 전체) |
| $\mu$ | `\mu` | 모평균 |
| $\sigma^2$ | `\sigma^2` | 모분산 |
| $\sigma$ | `\sigma` | 모표준편차 |
| $\bar{X}$ | `\bar{X}` | 표본평균 |
| $s^2$ | `s^2` | 표본분산 |
| $s$ | `s` | 표본표준편차 |
| $n$ | `n` | 표본 크기 (뽑은 데이터 개수) |

---

### 3.20 기호를 글자 그대로 쓰고 싶을 때

`*` 이나 `#` 를 서식이 아니라 글자로 보여 주려면 앞에 **역슬래시 `\`** 를 붙인다.

```md
\*별표\* 가 그대로 보인다.

\# 이건 제목이 아니다.

가격은 \$5 이다.
```

<div class="kicker">미리보기</div>

\*별표\* 가 그대로 보인다.

\# 이건 제목이 아니다.

가격은 \$5 이다.

<Callout kind="tip">
한글 키보드에서는 역슬래시가 <code>₩</code>(원화 기호)로 보이기도 한다. 같은 키다.
</Callout>

---

## 4. 자주 틀리는 것

| 증상 | 원인 | 고치는 법 |
|:--|:--|:--|
| `#제목` 이 그냥 글자로 나옴 | `#` 뒤에 공백 없음 | `# 제목` |
| 목록이 안 만들어짐 | `-`, `1.` 뒤에 공백 없음 | `- 항목` |
| 두 줄이 한 줄로 붙음 | 엔터를 한 번만 침 | 빈 줄 하나 넣기 |
| 하위 목록이 안 들어감 | 들여쓰기 칸 수가 다름 | 위 항목과 칸 수 맞추기 |
| 코드 블록이 끝나지 않음 | 닫는 역따옴표 세 개 빠짐 | 코드 끝에 ```` ``` ```` 추가 |

---

## 5. 실습하기 — 자기소개 페이지

<Grid cols="2">
<div>

<Steps color="ok">
<li><code>me.md</code> 파일을 만든다</li>
<li><code>#</code> 으로 이름을 제목으로 쓴다</li>
<li>좋아하는 것 세 가지를 목록으로 쓴다</li>
<li>이번 주 할 일을 체크박스로 쓴다</li>
<li>미리보기를 열어 오른쪽과 비슷하면 성공</li>
</Steps>

</div>
<div>

```md
# 홍길동

## 좋아하는 것

- 산책
- **음악 감상**
- 떡볶이

## 이번 주 할 일

- [x] VS Code 설치
- [ ] 마크다운 정리
```

</div>
</Grid>

---

## 6. 학습정리 — 한 장 요약

| 하고 싶은 것 | 쓰는 법 |
|:--|:--|
| 제목 | `# ` ~ `###### ` |
| 새 문단 | 빈 줄 하나 |
| 목록 | `1. ` · `- ` · `* ` |
| 강조 | `**굵게**` · `*기울임*` · `~~취소~~` |
| 링크 · 이미지 | `[글자](주소)` · `![설명](주소)` |
| 표 | `\| 칸 \| 칸 \|` + `\|---\|---\|` |
| 체크박스 | `- [ ] ` · `- [x] ` |
| 코드 | `` `한 줄` `` · ```` ```언어 ```` |
| 수식 | `$문장 속$` · `$$따로 한 줄$$` |

<span class="muted">기호 뒤 공백 한 칸과 빈 줄 하나, 이 두 가지만 지켜도 대부분 제대로 나온다.</span>

---

## 연습문제 — 고장 난 마크다운 고치기

아래는 `practice.md` 에 쓴 수업 노트인데 미리보기가 엉망으로 나온다. **틀린 곳 7군데**를 찾아 고쳐 보자.

<Grid cols="2">
<div>

```md
#마크다운 1일차 노트

## 오늘 한 일

1.VS Code 설치
    - 한국어 팩
  - Markdown All in One 익스텐션
1. **공식 홈페이지 둘러보기

## 점검

| 항목 | 상태 |
| 글자 크기 16 | 완료 |

-[x] practice.md 만들기
- [] 첫 코드 실행
```

</div>
<div>

<Steps color="ok">
<li>VS Code에서 <code>practice.md</code> 를 만들고 왼쪽 코드를 그대로 붙여 넣는다</li>
<li><code>Ctrl + K</code> → <code>V</code> 로 미리보기를 옆에 띄운다</li>
<li>미리보기를 보며 제목, 목록, 굵은 글씨, 표, 체크박스가 제대로 나올 때까지 고친다</li>
</Steps>

<Callout kind="tip" title="힌트">
대부분 <b>기호 뒤 공백 한 칸</b>, <b>들여쓰기 칸 수</b>, <b>짝이 맞지 않는 기호</b> 문제다. 막히면 <b>4. 자주 틀리는 것</b>과 <b>6. 학습정리</b>를 다시 본다.
</Callout>

</div>
</Grid>

---

### 연습문제 풀이

<Grid cols="2">
<div>

```md
# 마크다운 1일차 노트

## 오늘 한 일

1. VS Code 설치
    - 한국어 팩
    - Markdown All in One 익스텐션
1. **공식 홈페이지** 둘러보기

## 점검

| 항목 | 상태 |
|:--|:--|
| 글자 크기 16 | 완료 |

- [x] practice.md 만들기
- [ ] 첫 코드 실행
```

</div>
<div>

| 줄 | 고친 내용 |
|:--|:--|
| 1 | `#` 뒤에 공백 |
| 5 | `1.` 뒤에 공백 |
| 7 | 들여쓰기를 위 항목과 같은 4칸으로 |
| 8 | 닫는 `**` 추가 |
| 13 | 표의 구분 줄 `\|:--\|:--\|` 추가 |
| 16 | `-` 뒤에 공백 |
| 17 | `[ ]` 안에 공백 |

</div>
</Grid>
