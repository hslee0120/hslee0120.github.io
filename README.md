# hyungsuk-lee.github.io

개인 학술 웹사이트. GitHub Pages로 배포한다.

```
index.html   본문 전체 (섹션 구조만 고치면 됨)
style.css    스타일 (라이트/다크 자동, 모바일 대응, 인쇄용 포함)
cv/          CV PDF
```

---

## 배포 방법

### 1. GitHub에서 저장소 만들기

github.com에 로그인 → **New repository**

- **Repository name**: `hslee0120.github.io`
  예: 아이디가 `hyungsuklee`면 → `hyungsuklee.github.io`
- **Public** 선택
- README·.gitignore·license **추가하지 말 것** (빈 저장소로)

> 저장소 이름을 `hslee0120.github.io`로 하면 주소가 `https://hslee0120.github.io`가 된다.
> 다른 이름으로 만들면 `https://hslee0120.github.io/<저장소명>`이 된다.

### 2. 이 폴더를 올리기

이 폴더에서 터미널(Git Bash)을 열고:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/hslee0120/hslee0120.github.io.git
git push -u origin main
```

처음이면 이름·이메일을 먼저 설정한다:

```bash
git config --global user.name  "Hyungsuk Lee"
git config --global user.email "walden0230@gmail.com"
```

push 할 때 비밀번호를 물으면 **GitHub 계정 비밀번호가 아니라
Personal Access Token**을 넣어야 한다.
GitHub → Settings → Developer settings → Personal access tokens →
Tokens (classic) → Generate new token → `repo` 권한 체크 → 생성 후 복사.

### 3. Pages 켜기

저장소 → **Settings** → 왼쪽 **Pages**
- Source: **Deploy from a branch**
- Branch: **main** / **/ (root)** → Save

1~2분 뒤 `https://hslee0120.github.io` 로 열린다.

### 4. 이후 수정

```bash
git add .
git commit -m "Update publications"
git push
```

---

## 유지보수 메모

- **논문 추가**: `index.html`의 `<ol class="papers">` 안에 `<li>` 블록을 복사해서 수정
- **상태 표시**: `<span class="st">Revise and resubmit, ...</span>` — 붉은색으로 나온다
- **CV 교체**: `cv/CV_HyungsukLee.pdf`를 덮어쓰고 push
- 스타일은 `style.css` 맨 위 `:root` 변수만 바꿔도 색을 전부 바꿀 수 있다

## 하지 않은 것

- **논문 PDF는 저장소에 넣지 않았다.** 출판사 판본을 공개 저장소에 올리면
  저작권 문제가 생길 수 있다. 현재는 저널 공식 페이지(EER·FRB St. Louis Review는
  무료 공개)로 링크했다.
  개인 원고본을 올리고 싶으면 `papers/` 폴더를 만들어 넣고 링크를 걸면 된다.
  대부분의 저널이 **출판 전 원고(accepted manuscript)의 개인 사이트 게시는 허용**한다.
- 기존 Google Sites의 Dropbox 링크는 옮기지 않았다.
  Dropbox 링크는 만료될 수 있고, 실제로 `Asymmetric Credit Access` 링크는
  2026.09.07 기준 작동하지 않았다.
