#1. 리눅스 명령어
##가. top
####리눅스 시스템의 운용상황을 실시간으로 전반적인 상황을 모니터링하거나 프로세스 관리를 할 수 있는 유틸리티
##세부 정보 필드별 항목
####  PID USER  PR  NI  VIRT  RES  SHR S %CPU %MEM  TIME+  COMMAND
####    * PID : 프로세스 ID (PID)
####    * USER : 프로세스를 실행시킨 사용자 ID
####    * PRI : 프로세스의 우선순위 (priority)
####    * NI : NICE 값. 일의 nice value값이다. 마이너스를 가지는 nice value는 우선순위가 높음.
####    * VIRT : 가상 메모리의 사용량(SWAP+RES)
####    * RES : 현재 페이지가 상주하고 있는 크기(Resident Size)
####    * SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.
####    * S : 프로세스의 상태 [ S(sleeping), R(running), W(swapped out process), Z(zombies) ]
####    * %CPU : 프로세스가 사용하는 CPU의 사용율
####    * %MEM : 프로세스가 사용하는 메모리의 사용율
####    * TIME+ : 프로세스 시작된 이후 경과된 총 시간
####    * COMMAND : 실행된 명령어
    
    top 실행 전 옵션 : top의 정보들을 서식으로 출력하기 위한 옵션
    * -b		: 배치모드 옵션 
    * -n		: top 실행 주기를 설정
    * -p		: process ID 
     
    top 실행 후 사용할 수 있는 옵션
    * shift + t	: 실행된 시간이 큰 순서로 정렬
    * shift + m	: 메모리 사용량이 큰 순서로 정렬
    * shift + p	: cpu 사용량이 큰 순서로 정렬
    * k		: Process 종료
       o k 입력 후 종료할 PID를 입력한다
       o signal을 입력하라 표시되면 9를 넣어준다
    * c 		: 명령 인자 표시 / 비표시
    * l(소 문자엘) 	: uptime line(첫번째 행)을 표시 / 비표시
    * space bar	: Refresh
    * u		: 입력한 유저 소유의 Process만 표시
       o which user	: 와 같이 유저를 입력하라 표시될때 User를 입력
       o blank(공백) 입력시 모두 표시
    * shift + b	: 상단의 uptime 및 기타 정보값을 블락선택해 표시
    * f 		: 화면에 표시될 프로세스 관련 항목 설정
    * i			: idle 또는 좀비 상태의 프로세스는 표시 되지 않음
    * z		: 출력 색상 변경
    * d [sec]		: 설정된 초단위로 Refresh
    * c 		: command뒤에 인자값 표시
    * q		: 명령어 종료


나. ps

다. jobs

라. kill

2. vim 에디터에서 매크로 사용방법에 대하여 조사하기 (q , @)

 

- 조사한 내용을 자신의 github 페이지에 README 파일로 정리함


- 제출할 때는 github 페이지 링크와 pdf 파일을 같이 제시함
* github 페이지의 내용을 pdf 파일로 인쇄하여 같이 반드시 첨부할 것
* 마감기한 이후에 수정하는 것을 방지하기 위한...
* pdf 파일을 제시하지 않을 경우에는 과제 제출로 인정이 절대 안됨!!!
* 정확한 링크 주소를 제대로 안보낼 경우에는 감점 처리함
* 과제 제출 이후에는 commit과 push를 절대 수행하지 말 것

- 마감기한 : 2022년 6월 5일 (일), 23:59:59 까지

* 과제 점수는 10점이며, 지각제출은 불허입니다.

자세한 내용은 강의동영상 및 강의자료를 참고하길 바랍니다.
