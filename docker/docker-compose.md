# 컴포즈로 여러 컨테이너 실행하기

`docker-compose.yml` 파일을 작성하면 기존 `docker` 명령을 사용해 컨테이너를 실행할 때 매번 부여하던 옵션을 설정 파일로 관리할 수 있다. 이것만으로도 충분히 유용하지만, 컴포즈를 사용한 구성관리 기능의 진가는 여러 컨테이너를 실행할 때 발휘된다.



컴포즈를 사용해 여러 컨테이너를 실행하기 위해 필요한 기본 요소를 파악하기 위해 젠킨스(CI/CD 기능을 제공하는 서버 애플리케이션)를 예제 삼아 컴포즈로 실행해 보자.



## 젠킨스 컨테이너 실행하기

```dockerfile
version: "3"
services:
	master:
		container_name: master
		image: jenkinsci/jenkins:2.142-slim
		ports:
			- 8080:8080
		volums:
			- ./jenkins_home:/var/jenkins_home
```

젠킨스 이미지는 도커 허브에 올라와 있는 것을 이용한다.

`volumes` 항목은 호스트와 컨테이너 사이에 파일을 복사하는 것이 아니라 파일을 공유할 수 있는 메커니즘이다. `Dockerfile` 의 `COPY 인스트럭션` 이나 `docker container cp` 명령은 호스트와 컨테이너 사이에 파일을 복사하는 기능이었지만, `volumes` 는 공유라는 점에서 차이가 있다.
