# Scene Spec v1.4

Scene Spec는 내부 구조(Spec)와 외부 표현(Surface Prompt)을 분리하기 위한 기준 모델입니다.

## 목표
- UI 상태를 **Spec**으로 정규화한 뒤, 컴파일러가 Surface Prompt를 결정적으로 생성
- 모드(`SCENE_ONLY`, `PRODUCT_IN_SCENE`)에 따라 슬롯 사용 범위를 엄격히 제어
- Scene DNA 프리셋(팔레트/재질/빛/그레이딩/밀도/사진 톤)으로 스타일 일관성 유지
- Generate는 매번 최신 Spec에서 재컴파일하고 Gate로 pass/fail을 명시

## 운영 원칙
1. Spec는 단일 사실원(source of truth)이고 Prompt는 컴파일 산출물이다.
2. Surface Prompt는 콤마로 분리된 슬롯형 문자열을 사용한다.
3. `SCENE_ONLY`에서는 제품 슬롯을 출력하지 않는다.
4. `PRODUCT_IN_SCENE`에서는 placement/scale/brand moment 슬롯을 반드시 포함한다.
5. master ratio는 `{1:1, 3:2}`만 허용한다.
