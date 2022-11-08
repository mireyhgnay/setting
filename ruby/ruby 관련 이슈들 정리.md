# Ruby 관련 이슈들 정리하기

## 이슈1
**루비 설치 관련 오류화면**

![스크린샷 2021-01-07 오후 12.01.11.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d19fb0c6-62e3-4e23-91cb-318ea6a7547d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2021-01-07_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_12.01.11.png)

**해결방법 : ruby 버전 변경하여 에러 해결 → rbenv 설치**
```bash
# ruby 버전 확인 (ruby 2.7.2 이상 설치 필요)
$ ruby -v
 
# Homebrew 업데이트
$ brew update
 
# rbenv, ruby-build 설치
$ brew install rbenv ruby-build
 
# install 가능한 ruby 버전 확인
$ rbenv install —list
 
# rbenv 2.7.2 설치
$ rbenv install 2.7.2
 
# 설치 완료후 ruby 버전 확인
$ ruby -v
```

### 이슈2 : 2.7.2 버전으로 설치했지만 버전이 그대로인 경우

```bash
# ruby 버전 확인 : 버전 반영이 안됨
$ ruby -v
ruby 2.3.3p222 (2016-11-21 revision 56859) [universal.x86_64-darwin17]
 
# rbenv의 버젼 확인 : rbenv 버전은 제대로 반영되어 있음
$ rbenv versions
  system
* 2.7.2 (set by /Users/xxxx/.rbenv/version)
 
# ~/.bash_profile 파일 -> [eval "$(rbenv init -)"] 추가
$ vim ~/.bash_profile
 
# 추가후
$ source ~/.bash_profile
 
# ruby 버전 확인
$ ruby -v
 
 
# 또 안 된다면 아래 명령어 친 후
$ rbenv global 2.7.2
 
 
# ruby 버전 확인
$ ruby -v
```

### 이슈3 : rbenv 가 설치가 안되는 경우

```bash
# homebrew 버전 확인하기
$ brew -v
Homebrew 3.0.4
Homebrew/homebrew-core (no Git repository)
Homebrew/homebrew-cask (git revision fd93b5; last commit 2021-03-04)
 
# homebrew-core git clone 받기
$ git -C $(brew --repository homebrew/core) checkout master
 
# rbenv, ruby-build 설치
$ brew install rbenv ruby-build
 
# install 가능한 ruby 버전 확인
$ rbenv install —list
 
# rbenv 2.7.2 설치
$ rbenv install 2.7.2
 
# 설치 완료후 ruby 버전 확인
$ ruby -v
```