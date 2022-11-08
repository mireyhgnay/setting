## node 환경 설정 이슈

**이슈1. 404 Not Found - GET http://pkgrepos.tmon.net:8080/nexus/content/~~(이하생략) ~~/tmon-nexus-publish-0.0.6.tgz**

![MicrosoftTeams-image (2).png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b458458c-6907-494a-ad1d-9b5995ff87a0/MicrosoftTeams-image_(2).png)

원인

- 버전 노드모듈을 저장소에서 찾을 수 없음

해결 방법

- (추천) 방법1 : 모듈버전 변경
    - package.json > “nexus-publish” : “0.0.8”
- 방법2 : 모듈 주석처리
- 방법3 : npm install rimraf -g 오류 무시하고 설치
    - npm start || true ⇒ 오류 무시하고 실행

이슈2. mac os 버전에 따라 nvm 설치 중 아래와 같은 오류 발생

```bash
$ brew install nvm
Error: The following directories are not writable by your user:
/usr/local/share/man/man3
/usr/local/share/man/man5
/usr/local/share/man/man7
```

그럼 아래 내용 2개를 입력!

```bash
**sudo chown -R $(whoami) /usr/local/share/man/man3 /usr/local/share/man/man5 /usr/local/share/man/man7**
```

(맥 os 패스워드를 물어볼것이다)

```bash
**chmod u+w /usr/local/share/man/man3 /usr/local/share/man/man5 /usr/local/share/man/man7**
```

(이 글 작성 당시 node 버전 16.x.x 설치시 오래 발생!!  nvm 을 통해 11.15.0 으로 낮췄다)