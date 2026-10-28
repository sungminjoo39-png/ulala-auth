# web/ 폴더 — GitHub Pages에 올라가는 공개 파일

이 폴더 **안의 것만** GitHub에 올립니다. 올리는 방법: [../앱등록_안내.md](../앱등록_안내.md)

- `index.html` — App URL 로 쓰는 앱 소개 페이지
- `callback/index.html` — Redirect URI. 인증 코드를 보여주고 [복사하기] 버튼 제공
- `robots.txt` — 검색엔진 수집 차단

## 이 파일들에 없는 것

Client Secret · Access Token · Refresh Token · 인증 코드 — **한 글자도 없습니다.**
올리기 전에 직접 확인하세요:

```bash
.venv/bin/python ../scripts/업로드점검.py
```

## 콜백 페이지 보안

- `connect-src 'none'` — 인증 코드를 외부로 보내는 것이 기술적으로 불가능
- `default-src 'none'` — 외부 이미지·폰트·추적 스크립트 전부 차단
- `referrer: no-referrer` — 다른 사이트로 주소가 새지 않음
- 코드를 읽는 즉시 주소창에서 제거 — 방문 기록에 남지 않음
- 쿠키 · localStorage · sessionStorage 미사용
