| [Error] terminate called after throwing an instance of 'std::logic_error'

1. Error Content
terminate called after throwing an instance of 'std::logic_error'
  what():  basic_string::_M_construct null not valid
Aborted (core dumped)

개발 중 에러 메시지 발생

2. Reason
std::string or char* 에서 정의(허가)되지 않은 동작 사용 시 발생 되는 에러

3. Solution
배열(문자열)의 범위 외 데이터를 사용하였는지 확인, NULL 체크 확인 등
