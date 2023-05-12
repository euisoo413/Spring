##

### iBatis와 차이점
- `<sqlmap>` -> `<mapper>`
- `<sqlamp:(생략)>` -> `<mapper namespace="필수">`
- Alias를 사용하는 위치가 다르다. 
- resultmap 을 사용하지 못한다.
- `resultClass` -> `resultType` : 변화
- 변수 사용법이 바뀜 `#seq#` -> `#{seq}`
