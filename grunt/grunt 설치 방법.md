## grunt 설치 방법 

**저장소 clone받은 후,**

```bash
# pc 디렉토리로 이동
$ cd ...
 
# grunt 전역설치
$ npm install grunt -g
 
# npm 설치
$ npm install
 
# grunt 실행
$ grunt
```

### 최초 빌드

(**Gruntfile.js** 파일 확인 필요)

1. grunt default
2. grunt bswatch
3. src/html 과 src/scss 폴더 내 무작위 파일 새로고침
4. 3번 작업 시 src/htm_build 와 src/css 폴더 생성됨 => 산출물

### 이후 동작

**grunt bswatch** 실행