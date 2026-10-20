# events/

앱 인앱 웹뷰로 여는 이벤트 안내 페이지. 파일 1개 = 이벤트 1개(`events/<slug>.html`). 커밋·푸시하면 GitHub Pages가 1~2분 내 반영. 앱 안 이동 버튼은 `bbangmorning://bakery/<id>` 같은 앱 딥링크를 `<a href>`에 그대로 쓴다. 앱 로그인 정보는 페이지에 전달되지 않는다. 허용 호스트: event.bbangmorning.com(서버 AppConfig.inAppWebViewAllowedHosts).

## 앱 화면 연결 버튼 규칙
- 권장 딥링크: `bbangmorning://bakery/<id>`, `bbangmorning://market/product/<id>` — 웹뷰 위에 화면이 쌓이고 뒤로가기로 이벤트 페이지에 돌아온다.
- `bbangmorning://tab/*`, `home/*`, `challenge(s)` 는 웹뷰를 닫고 이동한다(2026-10-21 확정 동작). 이벤트 페이지로 되돌아와야 하면 쓰지 않는다.
- 허용 호스트 밖 https 는 외부 브라우저로 열린다. `tel:`·`mailto:` 만 외부 실행, 그 외 스킴은 무시된다.
- QA 페이지: `qa/webview-test.html`
