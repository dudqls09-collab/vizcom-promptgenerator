# Lint Rules v1.1

## 목적
코드 누출 및 금칙 패턴을 Generate 직전에 차단한다.

## 정책
- `reserved_tokens` 또는 `patterns`가 Prompt 문자열에서 감지되면 **Generate를 하드 차단**한다.
- 차단 시 UI에 발견된 토큰/패턴을 표시한다.
- v1.1에서는 자동 치환(autofix)을 하지 않는다.
  - 이유: 원인 추적과 규칙 정합성 검증이 우선이다.

## 적용 범위
- Generation Prompt
- Negative Prompt
- Revision Prompt

## 실패 처리
- 상태 메시지: `생성 차단: reserved token 누출(...)`
- Prompt 출력창은 갱신하지 않는다.
