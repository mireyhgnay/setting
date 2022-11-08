## Sass 설치 방법

```bash
$ gem install sass
```

**+) sass 설치 과정에서 위 명령어를 입력할 때 에러 발생**
```bash
ERROR: While executing gem ... 
(Gem::FilePermissionError)You don't have write permissions for the 
/Library/Ruby/Gems/2.6.0 directory.
```

와 같이 권한 문제로 sass 설치가 안될 경우 관리자 권한을 이용하는
`$ sudo gem install -n /usr/local/bin sass`를 입력합니다.