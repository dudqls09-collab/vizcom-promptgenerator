# v1.1 주요 기능 체크리스트 및 리빌드(v2) 대조 결과

## 1) v1.1 주요 기능 체크리스트
- [x] 옵션 섹션 (Scene / Camera / Product / Output 조작부)
- [x] 세그먼트(버튼형 선택 컨트롤)
- [x] 프리셋(씬 구성 프리셋 선택)
- [x] 저장/로드(사용자 상태 preset 저장 및 불러오기)
- [x] 출력 패널(생성 프롬프트/스펙 출력)
- [x] 게이트(검증 상태 표시)

## 2) 리빌드(v2) 항목별 대조

| 항목 | v2 상태 | 분류 | 조치 |
|---|---|---|---|
| 옵션 섹션 | 유지됨 | 유지 | 단일 상태 모델로 정리 |
| 세그먼트 | 유지됨 | 유지 | mode/ratio 모두 중복 ID 제거 |
| 프리셋(씬 구성) | 유지됨 (`Scene DNA Preset`) | 유지 | lexicon 기반 옵션 로딩 |
| 저장/로드 | 유지됨 (`Save Preset` / `Load Preset`) | 복구/안정화 | preset key를 v2 전용으로 분리 |
| 출력 패널 | 유지됨 (`Current Surface Prompt`, `Current Spec`) | 유지 | 단일 generate 파이프라인으로 통합 |
| 게이트 | 유지됨 (`Gate Status`) | 유지 | generate 시 항상 재평가 |
| 카메라 패드 | 유지됨 (`angle pad`) | 보강 | pitch/yaw 숫자 입력과 동기화 |
| Session Log Export | 유지됨 | 보강 | Markdown 다운로드로 분리 |

## 3) 최종 반영 원칙
- 깨진 `v1_2`를 봉합하기보다 `rebuild_v2`를 기준 UI로 사용.
- 기능 누락보다 구조 안정성(중복 ID 제거, 단일 바인딩)을 우선.
- `file://` 직접 실행 대신 로컬 서버 실행을 권장.
