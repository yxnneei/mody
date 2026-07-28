# MODY 모디 고객지원 페이지

앱스토어 등록에 필요한 "지원 URL(Support URL)"용 정적 웹사이트입니다.
빌드 도구 없이 순수 HTML/CSS로 작성되어 있어 아무 정적 호스팅에나 바로 올릴 수 있습니다.

## 구성

- `index.html` — 메인 지원 페이지 (문의, 계정 삭제 안내 / 개인정보처리방침 / 이용약관 링크)
- `delete-account.html` — 계정 삭제 안내
- `privacy.html` — 개인정보처리방침 (전문 포함)
- `terms.html` — 이용약관 (전문 포함)
- `styles.css` — 공통 스타일
- `assets/app-icon.png` — 앱 아이콘

개인정보처리방침·이용약관 내용을 수정할 때는 각 HTML 파일의 `<section class="card">`
블록을 직접 편집하세요.

## GitHub Pages로 배포하기 (추천)

1. GitHub에 새 저장소 생성 (예: `mody-support`)
2. 이 폴더 내용을 저장소에 push:
   ```bash
   cd mody-support
   git init
   git add .
   git commit -m "Add mody support site"
   git branch -M main
   git remote add origin https://github.com/<username>/mody-support.git
   git push -u origin main
   ```
3. GitHub 저장소 → **Settings > Pages** 로 이동
4. **Source**를 `main` 브랜치, `/ (root)` 폴더로 설정 후 저장
5. 몇 분 뒤 `https://<username>.github.io/mody-support/` 에서 사이트 확인
6. 이 URL을 App Store Connect의 "지원 URL(Support URL)" 항목에 입력

### 커스텀 도메인을 쓰고 싶다면

GitHub Pages 설정의 **Custom domain**에 원하는 도메인을 입력하고,
도메인 제공업체에서 해당 도메인의 DNS를 GitHub Pages로 연결하면 됩니다.
