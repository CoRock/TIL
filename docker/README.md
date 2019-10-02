# Docker

## [Dockerfile reference](https://docs.docker.com/engine/reference/builder/)

### What is instruction?

`Dockerfile` 에 전용 도메인 언어로 이미지의 구성을 정의한다.  `FROM` 이나 `RUN` 같은 키워드를 `인스트럭션(명령)` 이라고 한다.



### FROM Instruction

`FROM 인스트럭션` 은 도커 이미지의 바탕이 될 베이스 이미지를 지정한다. `Dockerfile` 로 이미지를 빌드할 때 먼저 `FROM 인스트럭션` 에 지정된 이미지를 내려받는다.

`FROM` 에서 받아오는 도커 이미지는 도커 허브(Docker Hub)라는 레지스트리* 에 공개된 것이다. 도커는 `FROM` 에서 지정한 이미지를 기본적으로 [도커 허브](https://hub.docker.com) 레지스트리에서 참조한다.

각 도커 이미지는 고유의 해시값을 갖는데, 이 해시만으로는 필요한 이미지가 무엇인지 특정하기가 어렵다. 특정 버전에 **태그**를 붙여두면 사람이 그 내용을 쉽게 파악할 수 있다.



### RUN Instruction

`RUN 인스트럭션` 은 도커 이미지를 실행할 때 컨테이너 안에서 실행할 명령을 정의하는 인스트럭션이다. 인자로 도커 컨테이너 안에서 실행할 명령을 그대로 기술한다.



### COPY Instruction

`COPY 인스트럭션` 은 도커가 동작 중인 호스트 머신의 파일이나 디렉터리를 도커 컨테이너 안으로 복사하는 인스트럭션이다.

`COPY` 와 기능이 비슷한 `ADD 인스트럭션` 도 있는데, `COPY` 와는 용도가 좀 다르다.



### CMD Instruction

`CMD 인스트럭션` 은 도커 컨테이너를 실행할 때 컨테이너 안에서 실행할 프로세스를 지정한다. `RUN 인스트럭션` 은 이미지를 빌드할 때 실행되고 `CMD 인스트럭션` 은 컨테이너를 시작할 때 한 번 실행된다. `RUN` 은 애플리케이션 업데이트 및 배치에, `CMD` 는 애플리케이션 자체를 실행하는 명령이라고 생각하면 된다.



### ENTRYPOINT Instruction

`ENTRYPOINT 인스트럭션` 을 사용하면 컨테이너의 명령 실행 방식을 조정할 수 있다.

`ENTRYPOINT` 는 `CMD` 와 마찬가지로 컨테이너 안에서 실행할 프로세스를 지정하는 인스트럭션이다.

`ENTRYPOINT` 를 지정하면 `CMD` 의 인자가 `ENTRYPOINT` 에서 실행하는 파일에 인자로 주어진다. 즉, `ENTRYPOINT` 에 지정된 값이 기본 프로세스를 지정하는 것이다.



### LABEL Instruction

이미지를 만든 사람의 이름 등을 적을 수 있다. 전에는 `MAINTAINER` 라는 인스트럭션도 있었으나 더 이상 사용하지 않는다(deprecated).



### ENV Instruction

도커 컨테이너 안에서 사용할 수 있는 환경변수를 지정한다.



### ARG Instruction

이미지를 빌드할 때 정보를 함께 넣기 위해 사용한다. 이미지를 빌드할 때만 사용할 수 있는 일시적인 환경변수다.



## Formulas

**도커 파일** = 서버 운영 기록 코드화

**도커 이미지** = 도커 파일 + 실행 시점

**도커 컨테이너** = 도커 이미지 + 환경변수

