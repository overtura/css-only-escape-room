# CSS-Only Escape Room

HTML과 CSS만으로 진행되는 퍼즐형 escape room입니다. 체크박스 상태, label, `:has()`, details를 조합해 런타임 JavaScript 없이 퍼즐 진행을 표현합니다.

## 목적
- CSS 상태 선택자로 게임형 interaction을 실험한다.
- no-JS 제약 안에서 재미있는 화면과 접근 가능한 진행 구조를 만든다.
- self-improving bot이 새 퍼즐, 문서, workflow 개선을 자동 PR로 제안하고 merge한다.

## 사용자 flow
1. 전등을 켜서 첫 단서를 찾는다.
2. 열쇠와 암호를 순서대로 활성화한다.
3. 세 상태가 모두 켜지면 출구가 열린다.

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
```bash
pnpm self-improve:context
pnpm self-improve:guard
```

## 범위 밖
- 런타임 JavaScript
- canvas/WebGL 게임 엔진
- 실제 secret 또는 credential 저장
