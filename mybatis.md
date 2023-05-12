### 
- https://mybatis.org/mybatis-3/ko 여기서 관련 정보 확인 가능


###
```
<!-- 스프링과 마이바티스 연동 설정 -->
<bean id="sqlSession" class="org.mybatis.spring.SqlSessionFactoryBean">
<!-- 위의 클래스는 스프링 기본 제공으로 사용한다. -->
	<property name="configLocation" value="classpath:sql-map-config(mybatis).xml"></property>
	<property name="dataSource" ref="dataSource"></property>
	<!-- 위의 데이타 소스는 게터세터로 가져온다... ibatis는 xml에 있었으나 지웠음 -->
</bean>

<bean class="org.mybatis.spring.SqlSessionTemplate">
	<property name=""></property>
</bean>

```
### 생성자 활용 (세터, 오토와이어드가 안되므로)
<img width="1049" alt="image" src="https://github.com/euisoo413/Spring/assets/63759241/5529fa50-3da7-422a-9190-79c691c59a42">

### `BoardDAOMybatis.java`에서 변경
<img width="800" alt="image" src="https://github.com/euisoo413/Spring/assets/63759241/e9284c9b-86a9-44ee-980c-26cb066eb3a0">

### namespace와 결합되어 요청 필요
<img width="893" alt="image" src="https://github.com/euisoo413/Spring/assets/63759241/ddf5e2da-b087-4bdb-8b45-08b630057b8f">


### iBatis와 차이점
- `<sqlmap>` -> `<mapper>`
- `<sqlamp:(생략)>` -> `<mapper namespace="필수">`
- Alias를 사용하는 위치가 다르다. 
- resultmap 을 사용하지 못한다.
- `resultClass` -> `resultType` : 변화
- 변수 사용법이 바뀜 `#seq#` -> `#{seq}`
