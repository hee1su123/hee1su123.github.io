# Cache

정의: 데이터 혹은 값을 미리 복사해 놓는 임시 장소. CPU와 주기억장치 사이에 위치하는 기억장치

사용 이유: CPU의 처리속도가 매우 빠른 속도로 성장한 반면, 메모리에 접근하는 속도는 이에 미치지 못했다. 아무리 CPU가 빨리 데이터를 처리해도, 데이터접근에 오랜 시간이 소요되어 이를 극복하기 위해 캐시를 사용

## Memory Hierarchy
- 메모리를 필요에 따라 여러가지 종류로 나누는 것을 말하며, CPU가 메모리에 더 빨리 접근하기 위해 사용한다
- 레지스터 < 캐시 < 메모리 < 하드 디스크 순으로 뒤로 갈수록 메모리가 크지만 접근속도가 느리다.

## Cache Hierarchy
- 메모리 계층에서 캐시에 해당하는 부분을 보통 3 부분으로 나누어 계층을 다시 한번 나눈다. L1, L2, L3 으로 구분한다

## 지역성
- 시간적 지역성: 반복문에 사용하는 조건 변수처럼 한번 참조된 데
이터는 또 참조될 가능성이 높음
- 공간적 지역성: A[0], A[1]과 같은 연속 접근 시, 참조된 데이터 근처에 있는 데이터가 또 사용될 가능성이 높음
- 해당 데이터뿐만 아니라, 옆 주소의 데이터도 같이 가져와 미래에
쓰일 것을 대비하기 위함

## Cache Hit & Miss
- Cache Hit & Miss: CPU가 요청한 데이터가 캐시에 있으면 Cache
Hit, 없어서 DRAM에서 가져오면 Cache Miss
- Cache Miss 종류
    - Cold Miss : 해당 메모리 주소를 처음 불러서 생김
    - Conflict Miss : A와 B가 같은 캐시 메모리 주소에 할당되어 생김
    - Capacity Miss : 캐시 메모리 공간 부족

## 캐시 작동 원리
- 추가 예정... 아직 정확하게 이해 하지 못한듯 하다..

## 캐시와 쿠키 차이점
- 추가