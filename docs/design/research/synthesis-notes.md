# Synthesis Notes

## Adopted Principles
- 퍼즐 진행은 card state와 door panel로 persistent하게 보여준다.
- 단서 활성화는 color, opacity, border, copy를 함께 사용한다.
- no-JS 제약을 사용자-facing 컨셉으로 드러낸다.

## Rejected Principles
- canvas/WebGL 게임 구현은 범위 밖이다.
- horror나 IP-specific visual clone은 쓰지 않는다.

## Token Changes
- `design-system/base.css`에 dark room puzzle token을 둔다.

## Golden Screens
- Initial locked room
- Lamp/key/code active sequence
- Door opened success state
