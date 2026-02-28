# Prompt Builder Rebuild Scope (v2)

## 목표
- 깨진 `ui/prompt_builder_mvp_v1_2.html`를 직접 봉합하지 않고, 안정 동작하는 기준선(`ui_prompt_builder.html`) 기반으로 재조립한다.
- 단일 상태 모델, 단일 액션 버튼 ID, 단일 출력 파이프라인으로 회귀 가능성을 줄인다.

## 재활용 자산
- 프롬프트 컴파일 파이프라인: `getSpec() -> compilePrompt() -> runGates()`
- 데이터 소스: `lexicon/room_placement_map.yml`, `lexicon/scene_dna.yml`, `lexicon/scale_buckets.yml`
- 핵심 UX: 모드 전환, ratio 프리뷰, placement custom 추가, gate 표시

## Must (이번 PR)
1. 작동하는 신규 HTML 엔트리 `ui/prompt_builder_rebuild_v2.html`
2. 중복 ID 제거 및 명시적 버튼 바인딩 (`generateBtn`, `savePresetBtn`, `loadPresetBtn`)
3. 프리셋 Save/Load + Reset + Session Log Export
4. Gate/Spec/Prompt 출력 정상 동작
5. 카메라 조작 UX(숫자 입력 + angle pad) 정상 동기화

## Should (다음 단계)
- 세션 로그에 PASS/FAIL 마킹 상세값 추가
- Revision Prompt/Negative Prompt를 feature flag로 분리
- 접근성 키보드 조작(arrow-key nudge) 강화

## 제외 범위 (이번 PR)
- 기존 `ui/prompt_builder_mvp_v1_2.html`의 레거시 코드 직접 수정
- 번들러/프레임워크 전환
