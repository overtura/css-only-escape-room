# Synthesis Notes

## Adopted Principles
- 퍼즐 진행은 card state와 door panel로 persistent하게 보여준다.
- 단서 활성화는 color, opacity, border, copy를 함께 사용한다.
- no-JS 제약을 사용자 facing 컨셉으로 드러낸다.
- 기본 토큰은 밝은 배경, 짙은 본문 텍스트, 흰색 card surface를 사용한다.

## Rejected Principles
- canvas/WebGL 게임 구현은 범위 밖이다.
- horror 또는 IP-specific visual clone은 쓰지 않는다.
- 검은 방 배경은 기본 방향에서 제외한다.

## Token Changes
- `design-system/base.css`에 bright puzzle desk token을 둔다.

## Golden Screens
- Initial locked room
- Lamp/key/code active sequence
- Door opened success state
