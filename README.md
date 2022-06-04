# 리눅스 명령어
## 1. top
#### 리눅스 시스템의 운용상황을 실시간으로 전반적인 상황을 모니터링하거나 프로세스 관리를 할 수 있는 유틸리티
### 1) 세부 정보 필드별 항목
![image](https://user-images.githubusercontent.com/97177686/172020504-d790a13d-5d37-415b-af5c-b6b15824a7ac.png)
#####  PID USER  PR  NI  VIRT  RES  SHR S %CPU %MEM  TIME+  COMMAND
######  PID : 프로세스 ID (PID)
######  USER : 프로세스를 실행시킨 사용자 ID
######  PRI : 프로세스의 우선순위 (priority)
######  NI : NICE 값. 일의 nice value값이다. 마이너스를 가지는 nice value는 우선순위가 높음.
######  VIRT : 가상 메모리의 사용량(SWAP+RES)
######  RES : 현재 페이지가 상주하고 있는 크기(Resident Size)
######  SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.
######  S : 프로세스의 상태 [ S(sleeping), R(running), W(swapped out process), Z(zombies) ]
######  %CPU : 프로세스가 사용하는 CPU의 사용율
######  %MEM : 프로세스가 사용하는 메모리의 사용율
######  TIME+ : 프로세스 시작된 이후 경과된 총 시간
######  COMMAND : 실행된 명령어
    
#### top 실행 전 옵션 : top의 정보들을 서식으로 출력하기 위한 옵션
|옵션|설명|
|:-----:|:-----|
| -b | 배치모드 옵션| 
| -n | top 실행 주기를 설정|
| -p | process ID |
     
#### top 실행 후 사용할 수 있는 옵션
|옵션|설명|
|:------:|:-----|
| shift + t	| 실행된 시간이 큰 순서로 정렬|
| shift + m	| 메모리 사용량이 큰 순서로 정렬|
| shift + p	| cpu 사용량이 큰 순서로 정렬|
| k| Process 종료(k 입력 후 종료할 PID를 입력한다)|
| c | 명령 인자 표시 / 비표시|
| l | uptime line(첫번째 행)을 표시 / 비표시|
| space bar	| Refresh|
| u | 입력한 유저 소유의 Process만 표시|
| shift + b	| 상단의 uptime 및 기타 정보값을 블락선택해 표시|
| f | 화면에 표시될 프로세스 관련 항목 설정|
| i	| idle 또는 좀비 상태의 프로세스는 표시 되지 않음|
| d [sec] | 설정된 초단위로 Refresh|
| q	| 명령어 종료|

## 2. ps
#### 현재 실행중인 프로세스를 보여주는 리눅스 명령어
![image](https://user-images.githubusercontent.com/97177686/172020555-11b454ef-3b31-4524-b968-86585fc27e9d.png)

|옵션|설명|
|:------:|:-----|
|-r | 현재 실행중인 프로세서를 보여줌|
|D | 디스크 입출력 대기 같은 인터럽트할 수 없는 대기상태 |
|T | 일시 정지 |
|-e | 모든 프로세스를 보여줌|
|-i | 상세내역을 보여줌|
|-ef | 모든 프로세스의 모든정보|

## 3. jobs
#### 작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경 되었지만 보고되지 않은 상태 등을 표시하는 명령어
### 옵션
|옵션|설명|
|:------:|:-----|
|-l| 프로세스 그룹 ID를 state 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p| 각 프로세스 ID에 대해 한 행씩 출력|
|command|지정한 명령어를 실행|

### jobs로 알 수 있는 세션의 상태 값
|상태|설명|
|:------:|:-----|
|Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임|
|Done|작업이 완료되어 0을 반환하고 종료 했음을 의미|
|Stopped|작업이 일시 중단|


## 4. kill
#### 프로세스를 죽일 때 사용
#### 내부적으로는 프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어

1. 시그널을 지정하지 않을 경우 기본 값인 정상 종료(15, SIGTERM) 시그널을 보냅니다.

` # kill [pid] `

2. 시그널 지정
```
 # kill -s [signal id] [pid]
 # kill -s [signal text] [pid]
 # kill -[signal id] [pid]
 # kill -[signal text] [pid] 
 ```

### 옵션
|옵션|설명|
|:------:|:-----|
|[pid] | 프로세스 ID|
|-l	| 사용 가능한 시그널 리스트 출력|
|-s | 시그널 지정|
|-1	-HUP | 프로세스를 재활성화|
|-15 |	프로세스 작업 종료|
|-9	| 프로세스 강제 종료|

------------

# vim 에디터 매크로
## vim 매크로
#### Vim 명령어들을 기록하고, 이를 반복할 수 있는 기능
## 매크로 사용방법 (q , @) (메크로 명은 A)
### q 메크로 사용 방법
|기능|vim키|
|:--|:--:|
|녹화 | qA |
|녹화 종료 | q|
|메크로 실행 | qA|

### 메크로 실행
`qA`

**3회 반복**
`3qA`

### 메크로 편집

`"Ap`

**편집한 내용 다시 등록**

`"Ayy`


### @ 메크로 사용 방법
|vim키|기능
|:--:|:--|
|@A | 1회 실행 |
|@@ | 방금 실행한 매크로 실행|
|10@A | 매크로 10회 실행|
