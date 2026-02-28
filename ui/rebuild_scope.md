# Prompt Builder Rebuild Scope (v3)

## 목표
- 실무자가 **옵션 버튼만 3~5회 선택**하면 프롬프트를 생성하고 복사해서 외부 생성형 플랫폼에서 즉시 제작할 수 있는 워크플로우를 만든다.
- 복잡한 설정 중심 UI를 버리고, **선택-생성-복사** 단일 경로를 기본 경험으로 고정한다.
- 실패 원인을 줄이기 위해 화면/상태/액션을 최소화한다.

## 공식 기준선(SSOT)
- 신규 기준 UI: `ui/prompt_builder_workflow_v3.html`
- 기존 파일 `ui_prompt_builder.html`, `ui/prompt_builder_mvp_v1_1.html`, `ui/prompt_builder_mvp_v1_2.html`, `ui/prompt_builder_rebuild_v2.html`는 reference-only로 취급한다.

## 핵심 사용자 여정 (Primary Journeys)
1. **Quick Generate (핵심)**
   공간/스타일/앵글 선택 → Generate → Copy → 외부 플랫폼 붙여넣기
2. **Fast Iterate (수정 반복)**
   옵션 1개만 변경 → 재생성 → 비교
3. **Directed Refinement (세부 지시)**
   추가 요청 텍스트 입력 → 생성 → 외부 제작

## IA (정보구조)
- **Option Selector**: 공간/스타일/앵글 버튼 그룹
- **Prompt Composer**: 선택값 + 추가 요청을 표준 문장 템플릿으로 합성
- **Output Console**: 생성 결과 확인/복사
- **Workflow Guide**: 실무 실행 순서와 KPI 표시

## Must (이번 PR)
1. 신규 엔트리 `ui/prompt_builder_workflow_v3.html`
2. 핵심 액션 버튼 3개로 축소 (`generateBtn`, `copyBtn`, `resetBtn`)
3. 버튼 기반 옵션 선택(공간/스타일/앵글)
4. 생성 결과 즉시 확인 + 복사 동작
5. 반응형 레이아웃(모바일 단일 컬럼)

## Should (다음 단계)
- 기존 lexicon/spec 컴파일러와 v3 단순 워크플로우를 어댑터로 연결
- 프리셋 저장/불러오기를 “팀 템플릿” 관점으로 재설계
- 실패 케이스(빈 출력, 복사 실패, 플랫폼별 길이 제한) UX 메시지 분기

## 제외 범위 (이번 PR)
- 레거시 v1/v2 파일 직접 수리
- 프레임워크 전환
- 인증/백엔드 저장소 도입
