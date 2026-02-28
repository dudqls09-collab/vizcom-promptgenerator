# Compile Rules v1.1 (Spec -> Surface Prompt)

1. 코드값(`*_code`)은 절대 직접 출력하지 않는다.
2. 코드값은 `lexicon/surface.yml`의 자연어 문구로 변환한다.
3. Prompt는 Vizcom 친화형 **comma-separated clause**로 구성한다.
4. 문장형보다 속성 나열형을 기본으로 한다.
5. clause 순서는 고정한다.
   - Scene
   - Subject(Product)
   - Placement/Keepout
   - Camera
   - Output(Crop-safe)
   - Brand Embrace
