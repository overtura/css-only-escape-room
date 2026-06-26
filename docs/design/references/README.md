# Design References

## Reference A
- Source/product: tactile puzzle interfaces
- Why selected: locked/unlocked state를 명확히 보여주는 방식을 참고한다.
- Principles to adopt: stateful objects, clear sequence, persistent success
- Elements not to copy: 특정 게임 IP, art style, asset identity
- Conflicts with our product: runtime game engine pattern은 제외한다.

## Reference B
- Source/product: compact board-game UI
- Why selected: grid 안에서 퍼즐 단계를 읽는 방식을 참고한다.
- Principles to adopt: contained playfield, action labels, visible inactive state
- Elements not to copy: board-game brand visuals
- Conflicts with our product: HTML/CSS-only 제약이 우선이다.
