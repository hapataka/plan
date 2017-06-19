## 하파타카 프레임워크(Hapataka framework) 프로젝트 목표

1. 시작하는 말

    많은 노드를 감시 통제하는 툴을 개발하는 프로젝트에 참여한 적이 있는데, 빅데이터 기술을 활용해서 메트릭 데이터의 저장, 색인, 검색등을 수행하고, 통계 및 AI 를 활용해서 메트릭 데이터 스트림에서 이상한 메트릭 데이터의 탐지등을 수행하는 툴을 개발했습니다. 그 프로젝트를 통해 습득한 기술과 아이디어는 다른 프로젝트에서도 유용하게 쓰일 수 있는 것 아닌가라는 생각에서 하파타카 프레임워크 프로젝트를 시작하게 됐습니다. 목표의 전체적인 내용에는, 여기 적혀 있는 기본적인 목표 이외에도 세세한 것이 많이 있지만, 프로젝트 대한 이해를 쉽게 하기 위해 기본적인 목표만을 추출하여 정리했습니다. 혹시, 독자 중에 이 목표와 관련해서 의견이 있으신 분이 계시다면, 어렵게 여기지 마시고 편하게 말씀해 주세요. (jhonsonchoi@gmail.com) 프로젝트의 기본적인 목표는 아래와 같습니다.

2. 전체

    2.1 개발자가 HTML, CSS, Javascript, Grpc 등 소수의 인기 기술을 활용해서 프론트엔드와 백엔드를 개발하면 풀스택 애플리케이션이 되어야 할 것.

    2.2. 개발 시, 사용자 수, 트랜잭션 수, 트래픽 양 등의 면에 대해서, 별 의식 없이 애플리케이션을 만들어도, 운용 시, 준수한 성능을 발휘하며 다양한 규모로 애플리케이션을 구축하여 운용할 수 있어야 할 것.

    2.3 클라이언트와 서버는 4가지 방식의 메세징이 가능하여야 할 것.

        하나의 요청 메세지에 하나의 응답 메세지
        하나의 요청 메세지에 스트림 형태의 다수의 응답 메세지
        스트림 형태의 다수의 요청 메세지에 하나의 응답 메세지
        스트림 형태의 다수의 요청 메세지에 스트림 형태의 다수의 응답 메세지.

    2.4 클라이언트와 서버에서 사용하는, 메세지 포맷은 JSON 을 사용하여, 개발자에게 친화적이어야 할 것.

    2.5 개발자나 운용자가 개발 및 운용에 관해 쉽게 이해할 수 있도록 필요한 자료를 제공할 것.

3. 클라이언트

    3.1 클라이언트는, 1개 이상의 플러그인 인스턴스들로 이루어져 있을 것. 

    3.2 플러그인 인스턴스는 플러그인 컨테이너에 배치되는데, 플러그인 컨테이너는, 플러그인 컨테이너 규격만 따른다면, 다른 단말기에 있을 수도 있고, 여러 개의 애플리케이션으로 구현돼도 무방할 것.

        예1) 사용자가 명령 입력기 같은 플러그인 인스턴스에서 명령을 입력하고 명령을 실행하도록 할 경우, 명령의 실행이나 명령 실행 결과의 조회는 다른 플러그인 인스턴스에서 이루어 질 수 있어야 할 것.
  
        예2) 다수의 플러그인 인스턴스가 하나의 컨테이너 인스턴스에 배치되는 것이 보통이지만, 다수의 컨테이너 인스턴스에 분리 배치될 수 있어야 할 것.
   
        예3) 핸드폰에서 실행 중인 명령 입력기에서 입력한 명령을 데스크탑에서 실행 중인 플러그인에서 실행하거나 결과 조회를 할 수 있어야 할 것.

    3.3 플러그인 인스턴스는 거주하는 플러그인 컨테이너에서 다른 컨테이너로 상태를 보존하며 이주할 수 있어야 할 것.

    3.4 플러그인은 HTML, CSS, Javascript 등으로 만들어져야 할 것. LESS, JSX 같은 것으로 작성된 소스가 트랜스파일된 것은 무방할 것.

    3.5 jquery 나 bootstrap 같은 것을 기반으로 개발된 것을 쉽게 플러그인으로 활용할 수 있어야 할 것.

    3.6 플러그인 컨테이너는 웹 브라우저는 물론 Electron, JXBrowser나 PhoneGap 같은 하이브리드 기술로도 구현되어야 할 것. 
     
    3.7 클라이언트는 데스크탑 애플리케이션과 비숫한 수준의 인터페이스를 제공할 수 있어야 할 것.

4. 서버
  
    4.1 서버는 쉽게 하지만 단순한 서비스부터 복잡한 서비스까지 구현할 수 있어야 할 것.
  
    4.2 서버는 성능이 준수하고 안정적인 서비스가 가능하야 할 것.
  
    4.3 서버는 다양한 언어 및 기술로 제작할 수 있어야 할 것.
   
    4.4 서버는 기존의 것을 쉽게 재활용할 수 있어야 할 것.
   
      
      
       
       
      