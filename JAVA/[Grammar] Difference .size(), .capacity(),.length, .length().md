| Difference. .size(), .capacity(),.length, .length() 

Outline.
개발하다 보면, 해당 배열의 크기가 필요하는 경우가 종종 생긴다.

이때 검색 혹은 TOOL을 이용하여 확인을 할텐데 size(), capacity(), length, length()등이 사용된다. 

그럼 이 네개의 차이는 어떤 것일까?

Difference.
size() Vector, List, Array List 등 Collection Type 길이 (원소 수)
capacity()	Vector, List, Array List 등 Collection Type 길이 (물리적 크기)
length 배열의 크기 (int, double, float...)
length() 문자열의 길이 

크게 네가지로 볼수 있다.

size와 capacity의 차이는 현재 가지고 있는 원소 수에 따른 결과 값과 이 실제 Collection타입에 변수에 할당 크기라고 보면된다.

length는 배열(Array)의 크기이며, length()는 사용되는 문자열의 길이를 나타내게 된다.
