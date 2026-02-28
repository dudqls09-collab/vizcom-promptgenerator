# Revision Prompt Template v1.2

한 번에 한 변수만 조정한다.

- Revision A (angle)
  - keep same scene, adjust camera in 5-degree steps near pitch {pitch} / yaw {yaw}.
- Revision B (props)
  - reduce foreground props near anchor zone and maintain clear staging clearance.
- Revision C (surface-readiness)
  - improve support-surface readability with subtle contrast and light focus while keeping a natural look.

규칙: 내부 코드(`scale_code`, `placement_code`) 문자열은 revision에도 포함하지 않는다.
