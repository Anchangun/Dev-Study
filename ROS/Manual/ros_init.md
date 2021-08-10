| ros::init()에 관하여

0. Where is ros::init()?
roscpp내에서 사용됨.

1. What is ros::init()?
요약 : roscpp사용 시 node에서 ROS Matster에게 현재 프로세스를 ros node로 등록하기 위해 사용됨

* roscpp 함수를 호출 하기전 하나의 ros::init은 있어야 함.

2. How is ros::init()?
2.1 설명

roscpp node 에서는 두가지 방법으로 초기화가 가능함.

2.1.1 ros::init()사용 노드 초기화

✓ 기본적인 사용

ros::init(argc, argv, "my_node_name");
구조 : int& argc, char** argv, const std::string& name

ros::init에 매개변수로 들어가는 int& argc, char** argv는 재매핑(Remapping)을 설정하는데 사용 됨.

* 평균적으로 main에서 받은 매개변수를 그대로 넣어줌.

name을 통하여 node name 설정

* 재매핑 시 동일한 노드 이름으로 할당하면 이전 노드는 자동으로 종료되며 여러개의 동일한 노드를 실행 하는 경우 아래와 같은 옵션을 사용.

✓ 옵션 사용

ros::init(argc, argv, "my_node_name", ros::init_options::AnonymousName);
구조 : int& argc, char** argv, const std::string& name, uint32_t option = 0

ros::init_options::NoSigintHandler : 노드가 종료되는 경우 올바르게 종료되도록 사용. 기능 처리 후 종료(SIGTERM)하려면 옵션 사용 하여야함.

* SIGINT Handler 설치 비추천

ros::init_options::AnnonymousName : 같은 노드를 다른 이름으로 사용할때 사용.

* 노드 이름 끝에 임의의 숫자를 추가하여 고유하게 만듬.

ros::init_options::NoRosout : /rosout 토픽에서 rosconsole로 브로드캐스트(전송) 하지 않게함.


✓ 재매핑 사용

void ros::init(<command line or remapping arguments>, std::string node_name, uint32_t options);
argc, argv를 사용하지 않고 재매핑 옵션을 사용하는 형태

std::map<std::string, std::string>, std::vector<std::string,std::string>을 사용할 수 있음.

ros::init() 호출 후 ros::master::check() 를 통하여 상태 확인 가능함.

2.1.2 ros::NodeHandle 생성을 통하여 초기화

자세한 내용은 차후 다른 문서를 통하여 게시

Reference Site :
http://docs.ros.org/en/api/roscpp/html/init_8h.html

http://wiki.ros.org/roscpp/Overview/Initialization%20and%20Shutdown
