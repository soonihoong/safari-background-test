# Mobile Safari Fullscreen Background Test

모바일 Safari 전체화면 배경 테스트를 위한 순수 HTML/CSS 정적 프로젝트입니다.

## 구성

- `index.html`: 테스트 페이지
- `images/background.png`: 전체화면 배경 이미지 경로
- `.gitignore`: macOS 기본 제외 항목

## 요구사항 반영 내용

- `viewport-fit=cover` 적용
- 배경 레이어 높이 `100lvh`
- 콘텐츠 영역 높이 `100dvh`
- `images/background.png`를 화면 전체 배경으로 사용
- 이미지 비율 무시 (`background-size: 100% 100%`)
- 기본 여백/스크롤 제거
- iPhone safe-area(`env(safe-area-inset-*)`) 대응
- 모바일 Safari 하단 툴바 영역까지 배경 확장
- GitHub Pages 호환 상대 경로 사용

## 실행 방법 (로컬)

먼저 원하는 이미지를 `images/background.png`로 저장합니다. 그다음 저장소 루트에서
`index.html`을 직접 열거나 아래처럼 간단한 정적 서버를 실행합니다.

```bash
python3 -m http.server 8000
```

브라우저에서 `http://localhost:8000`으로 접속합니다. 같은 네트워크의 iPhone에서
테스트하려면 `localhost` 대신 개발 컴퓨터의 로컬 IP 주소를 사용합니다.

## GitHub Pages 설정 방법

1. GitHub에 저장소를 생성하고 코드 푸시
2. 저장소의 **Settings > Pages** 이동
3. **Build and deployment**에서 Source를 **Deploy from a branch**로 설정
4. Branch를 `main` / `/ (root)`로 선택 후 저장
5. 배포 완료 후 제공되는 URL로 접속

## GitHub에 올리기

아래 명령에서 저장소 URL을 본인의 GitHub 저장소 URL로 바꿉니다.

```bash
git init
git add .
git commit -m "Add Mobile Safari background test page"
git branch -M main
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git push -u origin main
```

## 배경 이미지 준비

- `images/background.png` 파일을 원하는 이미지로 교체해주세요.
- 파일명과 경로는 반드시 동일하게 유지해주세요.
