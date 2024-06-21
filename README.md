이 파이썬 모듈은 주어진 관계가 동치 관계인지 확인하는 함수를 제공합니다.

# 함수들

## `check_reflexive(R, A)`
- 집합 A의 모든 요소 i에 대해 반복합니다.
- 관계 `R`이 반사적인지 확인합니다.
- `R`이 반사적이면 `True`를 반환하고, 아니면((i,i)가 관계 R에 포함되어 있지 않다면) `False`를 반환합니다.

## `check_symmetric(R)`
- 관계 R의 모든 쌍 (a, b)에 대해 반복합니다.
- 관계 `R`이 대칭적인지 확인합니다.
- `R`이 대칭적이면 `True`를 반환하고, 아니면((b, a)가 관계 R에 포함되어 있지 않다면) `False`를 반환합니다.

## `check_transitive(R)`
- 관계 R의 모든 쌍 (a, b)에 대해 반복합니다.
- 관계 R의 모든 쌍 (c, d)에 대해 반복합니다.
- 관계 `R`이 추이적인지 확인합니다.
- `R`이 추이적이면 `True`를 반환하고, 아니면(만약 b와 c가 같은데 (a, d)가 관계 R에 포함되어 있지 않다면) `False`를 반환합니다.

## `check_equivalence(R, A)`
- 관계 `R`이 동치 관계(반사적, 대칭적, 추이적 조건 모두 만족)인지 확인합니다.
- `R`이 동치 관계이면 `True`를 반환하고, 아니면 `False`를 반환합니다.

## 사용 예제

```python
from equivalence_relation import check_reflexive, check_symmetric, check_transitive, check_equivalence

A = {1, 2, 3, 4}  # 관계가 정의된 집합
R = {(1, 1), (1, 3), (2, 2), (3, 3), (3, 1), (3, 4), (4, 4), (4, 3)}  # 정의된 관계
print(f"반사적: {check_reflexive(R, A)}")
print(f"대칭적: {check_symmetric(R)}")
print(f"추이적: {check_transitive(R)}")
print(f"동치 관계: {check_equivalence(R, A)}")
