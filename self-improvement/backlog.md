# CSS-Only Escape Room 자가 개선 Backlog

체크박스와 CSS 선택자 기반 상태 흐름을 유지한다.

## Planning
- 퍼즐 추가 기준과 state progression 규칙을 `DESIGN.md`에 정리한다.
- no-JS 제약과 `:has()` fallback 설명을 문서화한다.

## Feature
- 기존 흐름을 깨지 않는 작은 새 clue 또는 rule 설명을 추가한다.
- 성공 상태 문구와 locked/opened 상태 설명을 개선한다.

## Design / Visual
- 밝은 puzzle desk 톤을 유지하면서 inactive card 대비를 개선한다.
- 모바일에서 puzzle card 간격과 action label 크기를 다듬는다.

## Accessibility
- hidden checkbox와 label 연결, door 상태 문구, heading hierarchy를 점검한다.
- color-only progress가 되지 않도록 텍스트 상태를 보강한다.

## Workflow
- self-improve PR body와 문서가 no-JS 게임 제약을 명확히 설명하도록 개선한다.
