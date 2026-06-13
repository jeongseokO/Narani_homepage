# Narani Homepage

[Narani](https://github.com/jeongseokO/Narani) — 에이전트와 나란히 개발하는 데스크톱 워크스페이스 — 소개 랜딩 페이지입니다.

단일 파일 정적 사이트입니다. `index.html` 하나만 열면 동작합니다(빌드 과정 없음).

## GitHub Pages로 배포하기

이 폴더의 내용을 `Narani_homepage` 저장소에 올리고 Pages를 켜면 됩니다.

### 1) 저장소에 올리기

이미 GitHub에 빈 저장소(`https://github.com/jeongseokO/Narani_homepage`)를 만들어 둔 상태라면, 이 폴더에서:

```bash
cd Narani_homepage
git init
git add .
git commit -m "랜딩 페이지 추가"
git branch -M main
git remote add origin https://github.com/jeongseokO/Narani_homepage.git
git push -u origin main
```

> 이미 로컬에 클론해 둔 저장소가 따로 있다면, 그 폴더에 `index.html`·`.nojekyll`만 복사한 뒤 `git add . && git commit && git push` 하면 됩니다.

### 2) Pages 켜기

1. GitHub에서 저장소 → **Settings** → 왼쪽 메뉴 **Pages**
2. **Build and deployment** → **Source**를 `Deploy from a branch`로
3. **Branch**를 `main` / `/ (root)`로 선택하고 **Save**
4. 1~2분 뒤 상단에 공개 주소가 뜹니다:
   **https://jeongseoko.github.io/Narani_homepage/**

`.nojekyll` 파일은 GitHub Pages가 밑줄(`_`)로 시작하는 파일·폴더를 무시하지 않도록 막아줍니다(나중에 에셋을 추가할 때를 위한 안전장치).

## 커스텀 도메인 (선택)

`narani.dev` 같은 도메인을 연결하려면:

1. 도메인 등록처(Cloudflare, Namecheap 등)에서 DNS에 `CNAME` 레코드를 `jeongseoko.github.io` 로 추가
2. 저장소에 도메인만 한 줄 적은 `CNAME` 파일을 추가하고 커밋
3. Settings → Pages → **Custom domain**에 도메인 입력 → **Enforce HTTPS** 체크

## 수정하기

`index.html` 한 파일에 HTML·CSS·JS가 모두 들어 있습니다. 텍스트·색(`:root`의 CSS 변수)·섹션을 바로 고치고 다시 push하면 1~2분 안에 반영됩니다.
