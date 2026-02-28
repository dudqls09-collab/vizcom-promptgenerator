# Rebuild Validation Checklist

## Phase 1: 기준 기능
- [x] Lexicon 로드 성공
- [x] Generate 클릭 시 Spec/Prompt 갱신
- [x] Gate Status 렌더링

## Phase 2: 상태/입출력 안정화
- [x] 중복 ID 없는 액션 버튼 구조
- [x] Save Preset / Load Preset 동작
- [x] Reset 동작
- [x] Session Log Export 동작

## Phase 3: UX 보강
- [x] PRODUCT_IN_SCENE 전환 시 placement controls 활성화
- [x] angle pad ↔ pitch/yaw 동기화
- [x] 반응형(1200px 이하 단일 컬럼) 레이아웃 유지

## 알려진 제약
- `file://` 직접 실행 시 `fetch('../lexicon/*.yml')`가 브라우저 정책으로 실패할 수 있음.
- 로컬 서버로 실행 권장 (`python3 -m http.server`).
