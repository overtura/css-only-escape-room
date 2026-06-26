# AGENTS.md

## Project Goal
이 저장소는 HTML/CSS만으로 진행되는 밝은 퍼즐형 escape room이다. self-improving bot은 작은 PR 단위로 퍼즐, 상태 문구, 접근성, fallback을 개선한다.

## Commands
- install: `pnpm install`
- dev: `pnpm dev`
- lint: `pnpm lint`
- build: `pnpm build`
- full check: `pnpm check`
- self-improve context: `pnpm self-improve:context`
- self-improve guard: `pnpm self-improve:guard`

## Done Definition
- 화면 문구는 기본적으로 한국어다.
- `index.html`과 build output에 런타임 `<script>`가 없다.
- checkbox와 CSS selector 기반 퍼즐 흐름이 실제로 동작한다.
- PR 요약에 검증 결과가 있다.

## Review Guidelines
- JavaScript state machine을 추가하지 않는다.
- hidden checkbox/label 연결, door 상태 문구, color-only progress를 우선 점검한다.
- self-improve 변경은 민감 정보 guard와 `pnpm check` 통과 여부를 먼저 본다.

## Self-Improve Loop Rules
- 반복 루프는 작은 PR 하나로 끝나야 한다.
- `self-improvement/backlog.md`의 후보를 우선 활용한다.
- 런타임 JavaScript, 실제 secret, API key는 추가하지 않는다.

## External Design Tool Rules
- UI 작업 전 `DESIGN.md`, `design-system/base.css`, no-JS 검증 규칙을 먼저 읽는다.
- `portfolio-design-tools-integration-pack`과 외부 디자인 레퍼런스는 참고 자료이며 source of truth가 아니다.
- 외부 브랜드의 정확한 로고, 폰트, 고유 composition을 복제하지 않는다.
- token 또는 shared component contract 변경은 별도 design-system 성격의 PR로 분리한다.
