# CSS-Only Escape Room

HTML과 CSS만으로 진행되는 퍼즐형 escape room입니다. 체크박스 상태, label, `:has()`, details를 조합해 런타임 JavaScript 없이 퍼즐 진행을 표현합니다.

## 목적
- CSS 상태 선택자로 게임형 interaction을 실험한다.
- no-JS 제약 안에서 재미있는 화면과 접근 가능한 진행 구조를 만든다.
- 중앙 maintainer bot이 새 퍼즐과 문서 개선을 target profile 기반 PR로 제안한다.

## 사용자 flow
1. 전등을 켜서 첫 단서를 찾는다.
2. 열쇠와 암호를 순서대로 활성화한다.
3. 세 상태가 모두 켜지면 출구가 열린다.

## 상태 흐름과 호환성
- `#lamp`, `#key`, `#code` 체크박스가 퍼즐 상태의 source of truth다.
- label이 체크박스를 토글하고, CSS `:has()` 선택자가 다음 카드와 출구 상태를 드러낸다.
- `:has()`를 지원하지 않는 브라우저에서는 단계별 잠금 해제가 보장되지 않는다. fallback을 추가할 때도 JavaScript state machine이 아니라 읽을 수 있는 HTML 문구와 CSS 기반 상태 표현을 우선한다.

## 실행 방법
```bash
pnpm install
pnpm dev
```

## 검증
```bash
pnpm check
```

`pnpm check`는 source와 build output 모두에서 런타임 JavaScript가 없는지 검사한다.

## 자가 개선
이 저장소에는 자가 개선 엔진을 두지 않는다. 중앙 control plane인 `okorion/self-improving-maintainer-bot`이 `profiles/overtura/css-only-escape-room.json` profile로 이 저장소를 target repo로 다룬다.

Target 설정은 `maintainer-bot/`에 둔다. 런타임 JavaScript, `.github/workflows/**`, credential, auth/security, infra, migration 변경은 R3로 취급하며 draft/proposal only로 처리한다.

## 디자인 시스템
- 기준 문서: `DESIGN.md`
- 실행 토큰: `design-system/base.css`
- 참고 기록: `docs/design/`

## 범위 밖
- 런타임 JavaScript
- canvas/WebGL 게임 엔진
- 실제 secret 또는 credential 저장
