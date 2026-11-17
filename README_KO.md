# PaperCal OAuth website — GitHub Pages

이 ZIP은 웹사이트 **초안**이다. 공개 전 실제 PaperCal의 데이터 처리와 개인정보처리방침 설명이 일치하는지 확인한다. 인증 토큰, Google OAuth client secret, events.json, 캘린더 데이터는 이 저장소에 올리지 않는다.

## GitHub Pages 게시 (도메인 구매 불필요)

1. GitHub에서 **새 Public repository** `papercal-oauth-site`를 만든다. (이미 같은 이름이 있으면 다른 이름 가능.)
2. ZIP을 풀어 `index.html`, `privacy.html`, `terms.html`, `style.css` 네 파일만 저장소 루트에 업로드한다. `README_KO.md` 파일 업로드는 선택 사항.
3. GitHub 저장소 **Settings > Pages > Build and deployment > Deploy from a branch > main / (root) > Save**.
4. GitHub Pages 주소를 확인한다: `https://YOUR_USERNAME.github.io/papercal-oauth-site/`
5. 홈페이지와 `privacy.html`, `terms.html`이 다른 브라우저에서도 로그인 없이 열리는지 확인한다.

## Google OAuth Branding

* Application home page: `https://YOUR_USERNAME.github.io/papercal-oauth-site/`
* Application privacy policy link: `https://YOUR_USERNAME.github.io/papercal-oauth-site/privacy.html`
* Terms of service: `https://YOUR_USERNAME.github.io/papercal-oauth-site/terms.html`
* Authorized domains: Google Cloud가 요청하는 **정확한 도메인**을 입력한다. 보통 `YOUR_USERNAME.github.io`지만 콘솔에서 `Domain not found`를 표시할 수도 있다. **`github.io`를 소유했다고 주장하지 않는다.** 실제 Google OAuth 검증은 Search Console 도메인 소유 증명을 요구할 수 있고 GitHub 하위 도메인은 제한될 수 있다.
* Logo: 없음 (선택)
* Contact email: 본인이 설정한 주소

Google Cloud에서 링크나 도메인을 거절하면 임의 도메인을 입력하지 않는다. 상태 화면의 정확한 오류를 확인하고 무료 호스팅/도메인 방식을 재검토한다.

Production으로 바꿔도 이전 Testing refresh token은 자동 복구되지 않는다. **기존 PaperCal outbox.json을 먼저 백업**하고 새로운 Google OAuth 재인증 후 pending 변경을 확인한다.

## Google 참고

- https://developers.google.com/identity/protocols/oauth2/policies
- https://developers.google.com/identity/protocols/oauth2
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://support.google.com/webmasters/answer/9008080
