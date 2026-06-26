# DESIGN.md - CSS-Only Escape Room

## Product Intent
HTML/CSS만으로 진행되는 시각 퍼즐형 escape room이다. 사용자는 checkbox 상태와 `:has()` 선택자만으로 램프, 열쇠, 암호, 출구 상태가 변하는 흐름을 경험한다.

## Design Authority
우선순위는 no-JS 제약, 이 문서, CSS semantic token, 외부 디자인 참고 순서다.

## Visual Character
```txt
Bright
Tactile
Puzzle-like
Readable
Contained
```

- 밝은 퍼즐 데스크 배경과 warm key light를 사용한다.
- amber는 진행 가능한 행동과 성공, cyan은 발견/활성 단서, red는 실패/위험에만 사용한다.
- game state는 색상 외에도 opacity, pointer behavior, text로 구분한다.
- 코드로 그린 간단한 UI는 허용하지만 placeholder처럼 보이면 안 된다.

## Typography
- UI: Inter, Pretendard, system-ui
- Display: 42-86px
- Puzzle title: 24-32px
- Body: 16-18px / 1.65
- Control: 14/20, bold

## Layout
- Intro와 playfield를 분리한다.
- Desktop은 4-column puzzle grid, tablet은 2-column, mobile은 1-column이다.
- Puzzle card radius는 8px 이하로 유지한다.

## Component Rules
- Puzzle card는 title, clue, action label을 포함한다.
- Hidden state는 읽을 수 있되 inactive임이 명확해야 한다.
- Success door는 persistent panel로 표시한다.
- runtime JavaScript나 canvas/WebGL 게임 엔진은 쓰지 않는다.

## Interaction Model
```txt
Lamp -> Key -> Code -> Door
```

## Anti-patterns
- JavaScript state machine
- inaccessible hidden controls
- color-only puzzle progress
- horror visual excess
- 검은 room shell
- external game brand clone
