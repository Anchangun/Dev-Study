| error : couldn't register subscriber on topic [/topic_name]

1. Outline

개발을 한참 하던 중, WARN 메세지가 떴다.

코드 상을 찾아봤는데 아무 문제가 없어 보여 당황하여 무엇을 놓쳤을지 보기 위해 topic_manager reference site를 들어가 확인해봤다.

TOPIC 등록하는 과정에서 문제가 생긴 듯한데 항상 짜던 subscribe 소스였기에 이해가 되지 않던 순간

TOPIC NAME을 상수화 시켜둔 헤더파일을 열어봤다.

define 하는 과정에서 실수로 내용을 지워버린 문제였다.



2. Solution
2.1 토픽 등록 하는 소스에서 문제가 없는지 확인.

2.2 토픽 이름 상수화 과정에서 문제 없었는지 확인.

위에 두가지라면 크게 문제없이 해결 될 것이다.



* 이런 실수는 하지 말자.



Reference Site :

http://docs.ros.org/en/indigo/api/roscpp/html/topic__manager_8cpp_source.html
