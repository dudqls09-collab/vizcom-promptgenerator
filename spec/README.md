# Scene Spec v1.1

Scene Spec는 내부 표현(코드)과 외부 표현(서피스 문구)을 분리하기 위한 기준 모델입니다.

## 목표
- 내부 코드(`room_code`, `time_code`, `mood_code`, `distance_code`, `lens_code`, `scale_code`, `placement_code`)는 UI/컴파일러 내부에서만 사용
- 생성 프롬프트에는 오직 서피스 문구(`room_desc`, `time_desc`, `mood_desc`, `distance_desc`, `lens_desc`, `scale_desc`, `placement_desc`, `keepout_desc`)만 사용
- 생성 직전 Lint Gate로 reserved token 누출을 하드 차단

## 운영 원칙
1. Spec는 사실(source of truth)이고 Prompt는 컴파일 산출물이다.
2. Prompt에 내부 코드 문자열이 등장하면 실패다.
3. Revision은 한 번에 한 변수만 조정한다.
