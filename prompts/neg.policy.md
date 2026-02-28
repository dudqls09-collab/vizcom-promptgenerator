# NEGATIVE POLICY v1.2

## 원칙
원치 않는 결과의 개념(사물/스타일)을 네거티브로 직접 언급하지 않는다.

- 이유: 특정 개념을 반복 언급하면 모델이 해당 개념을 강하게 활성화할 수 있다.
- 기본은 "말하지 않는 것"이다.
- 특히 Surface Prompt 본문에서는 제품명/제품군 같은 대상 키워드를 넣지 않는다.

## 허용 네거티브
A) Artifact only
- watermark
- signature
- text overlay
- gibberish text

B) Rule-violation 최소
- duplicated focal object
- clutter in anchor zone
- broken staging clearance

## 금지 네거티브
- 브랜드명/제품명/내부 코드/SKU/경쟁사/특정 오브젝트 나열형
- 제품 비노출 목적의 과도한 부정문 반복
