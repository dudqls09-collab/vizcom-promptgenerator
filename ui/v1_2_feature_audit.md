# v1.1 주요 기능 체크리스트 및 v1.2 대조 결과

## 1) v1.1 주요 기능 체크리스트
- [x] 옵션 섹션 (Scene / Camera / Product / Output 조작부)
- [x] 세그먼트(버튼형 선택 컨트롤)
- [x] 프리셋(씬 구성 프리셋 선택)
- [x] 저장/로드(사용자 상태 preset 저장 및 불러오기)
- [x] 출력 패널(생성 프롬프트/스펙 출력)
- [x] 게이트(검증 상태 표시)

## 2) v1.2 수정 후 항목별 대조 (1개씩 분류)

| 항목 | v1.2 상태 | 분류 | 조치 |
|---|---|---|---|
| 옵션 섹션 | 유지됨 | 유지 | 그대로 유지 |
| 세그먼트 | 유지됨 | 유지 | 그대로 유지 |
| 프리셋(씬 구성) | 유지됨 (`Scene DNA Preset`) | 유지 | 그대로 유지 |
| 저장/로드 | 복구 완료 (`Save Preset` / `Load Preset`) | 비의도삭제 → 복구 | 즉시 복구 반영 |
| 출력 패널 | 유지됨 (`Current Surface Prompt`, `Current Spec`) | 유지 | 그대로 유지 |
| 게이트 | 유지됨 (`Gate Status`) | 유지 | 그대로 유지 |
| quick angle preset | 제거 상태 | 의도삭제 | 최종 diff에 삭제 유지 |
| negative prompt | 제거 상태 | 의도삭제 | 최종 diff에 삭제 유지 |

## 3) 최종 diff 반영 원칙 점검
- 의도된 삭제만 잔존: quick angle preset, negative prompt.
- 비의도 삭제는 복구 완료: 저장/로드 기능.
