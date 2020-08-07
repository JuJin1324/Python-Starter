# Python-Starter


## Python 3.8
### Install
> macOS: `brew install python@3.8`   
> Ubuntu: `apt-get update; apt-get install -y python3` 

## Virtual Enviroment
### Install
> `pip install virtualenv`

### Set virtual enviroment
설정 명령어: `virtualenv --python=파이썬버전 가상환경이름`  
예시)
``` bash
$ mkdir python-virtual-test
$ cd python-virtual-test
$ virtualenv --python=3.8 venv
```

### 참조사이트
* [Virtualenv/VirtualenvWrapper OS별 설치&이용법](https://beomi.github.io/2016/12/28/HowToSetup-Virtualenv-VirtualenvWrapper/)

## Pip
### requirements.txt
* 프로젝트에 사용한 모듈 목록인 requirements.txt 생성하기: `pip freeze > requirements.txt`
* requirements.txt에 적힌 모듈 모두 다운받기: `pip install -r requirements.txt`

### 참조사이트
[[python] requirements.txt로 패키지 관리하기](https://itholic.github.io/python-requirements/)
