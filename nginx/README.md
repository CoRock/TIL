# Nginx

## 설정 파일의 역할

- `nginx.conf`: 메인 설정 파일
- `fcgi.conf`: FastCGI 환경설정 파일
- `sites-enabled`: 활성화된 사이트들의 설정 파일들이 위치. `Apache` 에서는 Virtual host의 설정에 해당한다. 기본적으로 존재하지 않을 수도 있다. 이 디렉터리를 직접 만들어서 사용하는 방법은 [가상 호스팅](https://opentutorials.org/module/384/4529)편에서 알아본다.
- `sites-available`: 비활성화된 사이트들의 설정 파일들이 위치



## References

- [NGINX Configuration](https://opentutorials.org/module/384/4526)
