## node 설치방법

```bash
$ brew update           //(필요시)brew 버전 최신화
 
$ brew install node     //node 설치
$ brew install nvm      //nvm 설치
 
 
$ brew -v       //잘 설치되었나 brew 버전 확인
$ node -v       //node 버전 확인
$ nvm -v        //nvm 버전 확인
 
 
$ nvm install 11.15.0       //node v11.15.0 설치
$ nvm list                  //잘 설치되었나 확인. 현재 설치되어 있는 node 버전 전부 보여줌
$ nvm uninstall 11.15.0     //(필요시)설치되어있지만 사용하지 않는 node 버전 제거
$ nvm use 11.15.0           //node v11.15.0로 현재 사용 버전 전환nvm
```