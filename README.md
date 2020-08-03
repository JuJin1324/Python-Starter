# Python-Starter


## Python 3.8
### Install
> macOS: `brew install python@3.8`   
> Ubuntu: `apt-get update; apt-get install -y python3.8`

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

## Syntax
### Indexing
* [:-1] : 가장 마지막 원소를 뺀 전부
* [Python 문자열 관련 함수.](http://egloos.zum.com/itbaby/v/4243381)

### 클래스 내부에서 클래스 자신의 타입 표시하기
class 선언시 내부 메서드에서 클래스 자신을 type hint 표시하면 에러 발생   
예시)
```python
class Url(object):
    short_url = ""
    full_url = ""

    @classmethod
    def shorten(cls, full_url: str) -> Url: # <- NameError: name 'Url' is not defined 에러 발생!
        instance = cls()
        instance.full_url = full_url
        instance.short_url = instance.__create_short_url()
        return instance
```
Python 4.0 이상인 경우 해당 문제는 발생하지 않는다.   
하지만 Python 4.0 이하의 경우 발생하며 최상단에 **from __future__ import annotations** 추가를 통해서 해결한다.   
[Stack overflow - How do I specify that the return type of a method is the same as the class itself?](https://stackoverflow.com/questions/33533148/how-do-i-specify-that-the-return-type-of-a-method-is-the-same-as-the-class-itsel)
