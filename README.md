# SPRING ADVANCED

## Lv0 에러 분석하기
<img width="1280" height="364" alt="image" src="https://github.com/user-attachments/assets/1fbe3b70-9641-4294-b08f-dd8f9bdcaa1b" />

→ application.yml 파일 만들어서 해결

## Lv1 ArgumentResolver
<img width="1646" height="804" alt="image" src="https://github.com/user-attachments/assets/3013f969-17c3-4829-a071-03523135949b" />

→  WebMvcConfig 클래스 만들어서 해결
WebMvcConfig가 없을 경우 AuthUserArgumentResolver는 Spring MVC에서 자동으로 사용되지 않음 


## Lv2 코드 개선
### 1) 코드 개선 퀴즈 - Early Return
<img width="1280" height="771" alt="image" src="https://github.com/user-attachments/assets/edeb7c74-9653-4f14-809f-fd9d193c28c4" />

→ encodedPassword 코드 위치 변경하여 해결

### 2) 리팩토링 퀴즈 - 불필요한 if-else 피하기
<img width="1280" height="707" alt="image" src="https://github.com/user-attachments/assets/07f99cc2-62d2-43f0-9dab-14fb7c2b6695" />

→ else문이 굳이 필요하지 않으므로 삭제하여 해결


### 3) 코드 개선 퀴즈 - Validation
<img width="1280" height="719" alt="image" src="https://github.com/user-attachments/assets/658e41de-9449-4be8-85f4-dc00028051e9" />

→ dto에 @Pattern을 이용해 Password 유효성 검증해서 해결


## Lv3 N+1 문제
JPQL fetch join을 사용하여 N+1 문제를 해결하고 있는 TodoRepository가 있습니다.
이를 동일한 동작을 하는 @EntityGraph 기반의 구현으로 수정해주세요.

→ @EntityGraph(attributePaths = {"user"})로 @EntityGraph 이용해서 해결


## Lv4 N+1 테스트코드
### 1) 테스트코드 연습
<img width="1280" height="524" alt="image" src="https://github.com/user-attachments/assets/e2d7a9d3-464b-4dca-bf15-f768ae231ff0" />

→ when 부분의 기본 비밀번호를 먼저 받고 인코딩된 비밀번호를 나중에 받아야 하므로 순서를 바꿔주어 해결

### 2-1) 테스트코드 연습
<img width="1280" height="267" alt="image" src="https://github.com/user-attachments/assets/ebb5fd4e-108d-4578-b84f-eb00d3783b5a" />
 → "Todo not found"라고 변경해서 해결


### 2-2) 테스트코드 연습
<img width="1280" height="738" alt="image" src="https://github.com/user-attachments/assets/bdae59ba-acb3-44d7-b2c1-93f35bd8b786" />
→ 테스트 코드 내의 저 Exception 부분을 ServerException로 수정해서 해결


### 2-3) 테스트코드 연습
<img width="1280" height="767" alt="image" src="https://github.com/user-attachments/assets/552c5ee0-208b-49ac-9f48-804195d96ddf" />

→ 만약 null일경우 InvalidRequestException을 던져주도록 Service 코드 부분에 추가해서 해결



