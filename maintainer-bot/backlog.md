# CSS-Only Escape Room Maintainer Bot Backlog

중앙 control plane은 `okorion/self-improving-maintainer-bot`이다. 체크박스와 CSS 선택자 기반 상태 흐름을 유지하고 런타임 JavaScript를 추가하지 않는다.

## 운영 검증
- 모든 변경은 `pnpm check`를 통과해야 한다.
- 자동 merge 기본값은 꺼져 있다.
- `.github/workflows/**`, credential, auth/security, infra, migration 변경은 R3로 취급하고 draft/proposal only로 다룬다.

## R0 Report
- 퍼즐 추가 기준과 state progression 규칙의 빈 부분을 분석 리포트로 정리한다.
- no-JS 제약과 `:has()` fallback 설명의 빈 부분을 정리한다.

## R1 PR 후보
- 기존 흐름을 깨지 않는 작은 새 clue 또는 rule 설명을 추가한다.
- 성공 상태 문구와 locked/opened 상태 설명을 개선한다.
- 밝은 puzzle desk 톤을 유지하면서 inactive card 대비를 개선한다.

## R2 Draft 후보
- build tooling, dependency, lint script 변경은 draft PR로만 제안한다.

## R3 Proposal only
- workflow, credential, security, infra, migration 관련 변경은 코드 변경 없이 proposal로만 다룬다.
